<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/items">Items</NuxtLink> &raquo;
        {{ item.Name }}
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
        <div id="stats" v-if="item">
          <div class="attr">
            STR: {{ item.Strength ? item.Strength : 0 }}<br/>
            CON: {{ item.Constitution ? item.Constitution : 0 }}<br/>
            INT: {{ item.Intelligence ? item.Intelligence : 0 }}<br/>
            LCK: {{ item.Luck ? item.Luck : 0 }}
          </div>
          <div class="attr">
            ATT1: {{ item.Attack ? item.Attack : 0 }}<br/>
            ATT2: {{ item.Attack2 ? item.Attack2 : 0 }}<br/>
            <br/>
            DEF : {{ item.Defense ? item.Defense : 0 }}
          </div>
          <div class="stats">
            <div v-if="item.DMG">Damage Type: {{ item.DMG }}</div>
            <div v-if="item.Speed">{{ item.Speed }} attack</div>
            <Found v-if="item.Found" :found="item.Found"/>
            <Dropped v-if="item.Dropped" :dropped="item.Dropped"/>
            <div v-if="item.Sold" style="margin-top:10px">Sold for ${{ item.Sold }}</div>
          </div>
          <div class="stats" v-if="item.Specials">
            Special moves:
            <div v-for="(special, index) in item.Specials" :key="index" class="special">
              <div>
                <img :src="require(`~/static/img/${special.Type}.gif`)" height="14"/>
              </div>
              ATT: {{ special.ATT ? special.ATT : 0 }} MP: {{ special.MP ? special.MP : 0 }}<br/>
              {{ special.Info }}
            </div>
          </div>
        </div>
        <div id="stats"v-else></div>
        <div id="info" v-if="item">
          <div style="float:left"><img :src="require(`~/assets/items/${slugify(item.Name)}.gif`)" width="56"/></div>{{ item.Description }}
        </div>
        <div id="info" v-else></div>
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
        item: ''
      }
    },
    mounted() {
      this.item = this.$store.getters.item(this.$route.params.item.replace(/-/g,' '));
      if(process.client) {
        let el = document.getElementById(this.item.Name);
        el.scrollIntoView({block: 'center', behavior: 'auto'});
      }
    },
    computed: {
      selected() {
        return this.$store.getters.item(this.item);
      }
    },
    methods: {
      slugify(str) {
        return str.toLowerCase().replace(/ /g, '-');
      },
      found(found) {
        let maps = ['Entrance','Alchemy Laboratory','Marble Gallery','Outer Wall','Long Library','Clock Tower','Royal Chapel','Castle Keep','Colosseum','Olrox\'s Quarters','Underground Caverns','Abandoned Mine','Catacombs'];
        found = found.map(map => {
          if(maps.includes(map)) return `<a href="/maps/${map.replace(/ /g,'-')}">${map}</a>`;
          return map;
        });
        return found.join(', ');
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
  #inventory a:hover {
    height: 31px;
    border-style: solid;
    border-width: 2px;
    color: #fff;
  }
  #inventory a:active, .nuxt-link-exact-active {
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