<template>
  <table id="enemy">
    <tr>
      <td colspan="4"><img v-if="enemy.Blood" src="/img/blood.gif" title="Blood" alt="Blood"/><img v-else src="/img/skelly.gif" title="No blood" alt="No blood"/>{{ enemy.Name }}</td>
      <td style="width: 255px; text-align: right">No. {{ enemy.ID }}</td>
    </tr>
    <tr>
      <td style="width: 100px;">LV <span id="lv">{{ enemy.LV }}</span></td>
      <td style="width: 100px;">HP {{ enemy.HP }}</td>
      <td colspan="2">Strong VS.</td>
      <td rowspan="7">
        <div style="height: 241px; line-height: 29px; overflow: auto;">
          Found in:
          <ul>
            <li v-for="(found, index) in enemy.Found" :key="index" v-if="maps.includes(found)"><NuxtLink :to="`/maps/${found.replace(/ /g,'-').replace(/'/g,'')}`">{{ found }}</NuxtLink></li>
            <li v-else>{{ found }}</li>
          </ul>
          <div v-if="attacks.length">
            Attacks:
            <ul><li v-for="attack in attacks">{{ attack.Name }}: ATT {{ attack.ATT }} {{ attack.Type }}</li></ul>
          </div>
        </div>
      </td>
    </tr>
    <tr>
      <td>STR {{ enemy.STR }}</td>
      <td>DEF {{ enemy.DEF }}</td>
      <Element :element="enemy.Strong"/>
    </tr>
    <tr>
      <td colspan="2" rowspan="8" align="center"><img width="192" :src="require(`~/assets/enemies/${slugify(enemy.Name)}.png`)" alt="Enemy picture"/></td>
      <td colspan="2">Immune</td>
    </tr>
    <tr><Element :element="enemy.Immune"/></tr>
    <tr><td colspan="2">Weak VS.</td></tr>
    <tr><Element :element="enemy.Weak"/></tr>
    <tr><td colspan="2">Absorbs</td></tr>
    <tr><Element :element="enemy.Absorb"/><td>Drop Items:</td></tr>
    <tr>
      <td style="width: 100px;">Your Level: </td>
      <td><input type="number" min="1" max="99" v-model.number="lv" style="width: 32px;"/></td>
      <td v-if="enemy.Drop1">
        <NuxtLink :to="`/items/${enemy.Drop1.replace(/ /g,'-')}`"><img :src="require(`~/assets/items/${slugify(enemy.Drop1)}.gif`)" width="20" alt=""/>{{ enemy.Drop1 }}</NuxtLink>
      </td>
      <td v-else class="none">None</td>
    </tr>
    <tr>
      <td>EXP: </td>
      <td><span id="exp">{{ givenExp }}</span></td>
      <td v-if="enemy.Drop2">
        <NuxtLink :to="`/items/${enemy.Drop2.replace(/ /g,'-')}`"><img :src="require(`~/assets/items/${slugify(enemy.Drop2)}.gif`)" width="20" alt=""/>{{ enemy.Drop2 }}</NuxtLink>
      </td>
      <td v-else class="none">None</td>
    </tr>
    <tr><td colspan="5" style="height: 64px; font-size: 24px;">{{ enemy.Description }}</td></tr>
  </table>
</template>

<script>
  export default {
    props: ['enemy'],
    data() {
      return {
        lv: 0,
        maps: ['Entrance','Alchemy Laboratory','Marble Gallery','Outer Wall','Long Library','Clock Tower','Royal Chapel','Castle Keep','Colosseum','Olrox\'s Quarters','Underground Caverns','Abandoned Mine','Catacombs']
      };
    },
    methods: {
      slugify(str) {
        return str.toLowerCase().replace(/ /g, '-');
      },
    },
    computed: {
      attacks() {
        return this.$store.getters.attacks(this.$route.params.enemy);
      },
      givenExp() {
        let exp = Math.pow(2/3, this.lv-this.enemy.LV) * this.enemy.EXP;
        if (exp < 1) return 1;
        if (exp > 9999) return 9999;
        if (this.lv < this.enemy.LV) exp = Math.pow(3/4, this.lv-this.enemy.LV) * this.enemy.EXP;
        return isNaN(exp) ? 0 : parseInt(exp);
      }
    },
    created() {
      this.lv = this.enemy.LV;
    },
    transition: 'enemy'
  }
</script>

<style scoped>
  ul{
    margin: 0;
  }
  #enemy{
    background: linear-gradient(#550, #500);
    width: 700px;
    line-height: 31px;
    border: solid;
    padding: 5px;
  }
  .none{
    color: #f90;
  }
  .element{
    color: #0f0;
  }
  .enemy-enter-active, .enemy-leave-active {
    transition: transform .5s;
  }
  .enemy-enter, .enemy-leave-to {
    transform: scaleX(0);
  }
</style>