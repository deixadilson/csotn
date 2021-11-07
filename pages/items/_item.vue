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
        <p>The full list of items and relics.</p>
        <Inventory/>
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
    head() {
      return {
        title: `${this.item.Name} - Castlevania: Symphony of the Night`
      }
    },
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
    methods: {
      slugify(str) {
        return str.toLowerCase().replace(/ /g, '-');
      }
    }
  }
</script>

<style scoped>
  p{
    text-align: center;
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
  #stats, #info{
    background: linear-gradient(#020223, #1d1d5c);
  }
</style>