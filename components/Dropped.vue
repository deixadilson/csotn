<template>
  <div>
    Dropped by:<br/>
    <NuxtLink v-for="(enemy, index) in dropped" :key="index" :to="`/enemies/${enemy.replace(/ /g,'-')}`">{{ enemy }}</NuxtLink>
  </div>
</template>

<script>
  export default {
    props: ['dropped']
  }
</script>

<style scoped>
  div {
    margin-top: 10px;
  }
  a:after {
    content: ', ';
    color: #fff;
    font-weight: normal;
  }
  a:last-child:after {
    content: '';
  }
</style>