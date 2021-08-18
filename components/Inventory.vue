<template>
  <div>
    <NuxtLink v-for="(i, index) in this.$store.state.items" :key="index" :to="`/items/${i.Name.replace(/ /g,'-')}`" :id="i.Name">
      <img :src="require(`~/assets/items/${slugify(i.Name)}.gif`)" :to="`/items/${i.Name}`" width="28"/>{{ i.Name }}
    </NuxtLink>
  </div>
</template>

<script>
  export default {
    methods: {
      slugify(str) {
        return str.toLowerCase().replace(/ /g, '-');
      }
    }
  }
</script>

<style scoped>
  div{
    width: 300px;
    height: 400px;
    padding: 4px;
    border-style: solid;
    margin-left: 54px;
    float: left;
    overflow: auto;
    background: linear-gradient(#020223, #1d1d5c);
  }
  a{
    height: 35px;
    display: block;
  }
  a:hover{
    height: 31px;
    border-style: solid;
    border-width: 2px;
    color: #fff;
  }
  a:active, .nuxt-link-exact-active{
    background-color: #a00;
    color: #fff;
  }
</style>