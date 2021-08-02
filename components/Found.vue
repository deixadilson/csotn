<template>
  <div>
    Found in:<br/>
    <NuxtLink v-for="(map, index) in found" :key="index" v-if="maps.includes(map)" :to="`/maps/${map.replace(/ /g,'-').replace(/'/g,'')}`">{{ map }}</NuxtLink>
    <span v-else>{{ map }}</span>
  </div>
</template>

<script>
  export default {
    props: ['found'],
    data() {
      return {
        maps: ['Entrance','Alchemy Laboratory','Marble Gallery','Outer Wall','Long Library','Clock Tower','Royal Chapel','Castle Keep','Colosseum','Olrox\'s Quarters','Underground Caverns','Abandoned Mine','Catacombs']
      }
    }
  }
</script>

<style scoped>
  div {
    margin-top: 10px;
  }
  a:after, span:after {
    content: ', ';
    color: #fff;
    font-weight: normal;
  }
  a:last-child:after, span:last-child:after {
    content: '';
  }
</style>