<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        Items
      </div>
      <Header/>
      <h2>Items</h2>
      <hr/>
      <main>
        <p style="text-align: center">The full list of items and relics.</p>
        <div id="inventory">
          <NuxtLink v-for="(i, index) in this.$store.state.items" :key="index" :to="`/items/${i.Name.replace(/ /g,'-')}`" :id="i.Name">
            <img :src="require(`~/assets/items/${slugify(i.Name)}.gif`)" :to="`/items/${i.Name}`" width="28"/>{{ i.Name }}
          </NuxtLink>
        </div>
        <div id="stats"></div>
        <div id="info"></div>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        classes: ['S.Sword','Sword','Throw 1','Fist','Club','Two-hand','Shield','Throw 2','Bomb','Medicine','Food','Head','Armor','Cloak','Other','Relic'],
        selected: ''
      }
    },
    computed: {
      selected() {
        return this.$store.getters.item(this.selected);
      }
    },
    methods: {
      slugify(str) {
        return str.toLowerCase().replace(/ /g, '-');
      },
      dropped(dropped) {
        dropped = dropped.map(enemy => `<a href="/enemies/${enemy.replace(/ /g,'-')}">${enemy}</a>`);
        return dropped.join(', ');
      }
    }
  }
</script>

<style scoped>
  #inventory{
    width: 300px;
    height: 400px;
    padding: 4px;
    border-style: solid;
    margin-left: 54px;
    float: left;
    overflow: auto;
  }
  #inventory a{
    height: 35px;
    display: block;
  }
  #inventory a:hover{
    height: 31px;
    border-style: solid;
    border-width: 2px;
    color: #fff;
  }
  #inventory a:active{
    background-color: #a00;
    color: #fff;
  }
  #stats{
    width: 300px;
    height: 400px;
    padding: 4px;
    border-style: solid;
    border-left: 0;
    text-align: left;
    line-height: 125%;
    float: left;
  }
  .attr{
    float: left;
    width: 140px;
    font-family: monospace;
    margin: 0 5px 10px;
  }
 .stats{
    margin: 0 5px 10px;
  }
  .special {
    margin: 2px 0 10px;
  }
  #info{
    width: 600px;
    height: 65px;
    border-style: solid;
    border-top: 0;
    padding-right: 19px;
    margin-left: 54px;
    clear: left;
  }
  #inventory, #stats, #info{
    background: linear-gradient(#020223, #1d1d5c);
  }
</style>