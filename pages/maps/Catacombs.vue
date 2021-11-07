<template>
  <div class="wrapper">
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/maps">Maps</NuxtLink> &raquo;
        Catacombs
      </div>
      <Header/>
      <h2>Catacombs</h2>
      <hr/>
      <main>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/31,100.gif"/><img src="/img/maps/rload.gif"/><br/>
        <img src="/img/maps/16,101.gif"/><img src="/img/maps/17,101.gif"/><img src="/img/maps/18,101.gif"/><img src="/img/maps/19,101.gif"/><img src="/img/maps/20,101.gif"/><img src="/img/maps/21,101.gif"/><img src="/img/maps/bsave.gif"/><img src="/img/maps/23,101.gif"/><img src="/img/maps/24,101.gif"/><img src="/img/maps/25,101.gif"/><img src="/img/maps/26,101.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/28,101.gif"/><img src="/img/maps/29,101.gif"/><img src="/img/maps/bsave.gif"/><img src="/img/maps/31,101.gif"/><img src="/img/maps/32,101.gif"/><img src="/img/maps/33,101.gif"/><img src="/img/maps/34,101.gif"/><img src="/img/maps/35,101.gif"/><img src="/img/maps/36,101.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/38,101.gif"/><img src="/img/maps/39,101.gif"/><img src="/img/maps/40,101.gif"/><img src="/img/maps/41,101.gif"/><img src="/img/maps/42,101.gif"/><img src="/img/maps/43,101.gif"/><img src="/img/maps/44,101.gif"/><img src="/img/maps/45,101.gif"/><img src="/img/maps/46,101.gif"/><img src="/img/maps/47,101.gif"/><img src="/img/maps/48,101.gif"/><br/>
        <img src="/img/maps/16,102.gif"/><img src="/img/maps/17,102.gif"/><img src="/img/maps/18,102.gif"/><img src="/img/maps/19,102.gif"/><img src="/img/maps/20,102.gif"/><img src="/img/maps/21,102.gif"/><img src="/img/maps/22,102.gif"/><img src="/img/maps/23,102.gif"/><img src="/img/maps/24,102.gif"/><img src="/img/maps/25,102.gif"/><img src="/img/maps/26,102.gif"/><img src="/img/maps/27,102.gif"/><img src="/img/maps/28,102.gif"/><img src="/img/maps/29,102.gif"/><img src="/img/maps/30,102.gif"/><img src="/img/maps/31,102.gif"/><img src="/img/maps/32,102.gif"/><img src="/img/maps/30,102.gif"/><img src="/img/maps/31,102.gif"/><img src="/img/maps/35,102.gif"/><img src="/img/maps/36,102.gif"/><img src="/img/maps/37,102.gif"/><img src="/img/maps/38,102.gif"/><img src="/img/maps/39,102.gif"/><img src="/img/maps/40,102.gif"/><img src="/img/maps/41,102.gif"/><img src="/img/maps/42,102.gif"/><img src="/img/maps/43,102.gif"/><img src="/img/maps/44,102.gif"/><img src="/img/maps/45,102.gif"/><img src="/img/maps/46,102.gif"/><img src="/img/maps/47,102.gif"/><img src="/img/maps/48,102.gif"/>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<style scoped>
  img {
    vertical-align: bottom;
  }
  .wrapper, .container {
    width: max-content;
  }
</style>

<script>
  export default {
    head() {
      return {
        title: 'Catacombs - Castlevania: Symphony of the Night'
      }
    }
  }
</script>