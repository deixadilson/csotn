<template>
  <NuxtLink :to="`/items/${item.replace(/ /g,'-')}`"><img :src="require(`~/assets/items/${item.replace(/ /g,'-').toLowerCase()}.gif`)" alt=""/>{{ item }}</NuxtLink>
</template>

<script>
  export default {
    props: ['item']
  }
</script>

<style scoped>
  a {
    white-space: nowrap;
  }
</style>