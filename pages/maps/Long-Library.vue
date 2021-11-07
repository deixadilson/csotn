<template>
  <div class="wrapper">
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/maps">Maps</NuxtLink> &raquo;
        Long Library
      </div>
      <Header/>
      <h2>Long Library</h2>
      <hr/>
      <main>
        <img src="/img/maps/44,69.gif"/><img src="/img/maps/45,69.gif"/><img src="/img/maps/46,69.gif"/><img src="/img/maps/47,69.gif"/><img src="/img/maps/48,69.gif"/><img src="/img/maps/49,69.gif"/><img src="/img/maps/50,69.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/52,69.gif"/><img src="/img/maps/53,69.gif"/><img src="/img/maps/54,69.gif"/><img src="/img/maps/55,69.gif"/><img src="/img/maps/56,69.gif"/><img src="/img/maps/57,69.gif"/><img src="/img/maps/58,69.gif"/><img src="/img/maps/59,69.gif"/><br/>
        <img src="/img/maps/44,70.gif"/><img src="/img/maps/45,70.gif"/><img src="/img/maps/46,70.gif"/><img src="/img/maps/47,70.gif"/><img src="/img/maps/48,70.gif"/><img src="/img/maps/49,70.gif"/><img src="/img/maps/50,70.gif"/><img src="/img/maps/bsave.gif"/><img src="/img/maps/52,70.gif"/><img src="/img/maps/53,70.gif"/><img src="/img/maps/54,70.gif"/><img src="/img/maps/55,70.gif"/><img src="/img/maps/56,70.gif"/><img src="/img/maps/57,70.gif"/><img src="/img/maps/58,70.gif"/><img src="/img/maps/59,70.gif"/><br/>
        <img src="/img/maps/44,71.gif"/><img src="/img/maps/45,71.gif"/><img src="/img/maps/46,71.gif"/><img src="/img/maps/47,71.gif"/><img src="/img/maps/48,71.gif"/><img src="/img/maps/49,71.gif"/><img src="/img/maps/50,71.gif"/><img src="/img/maps/51,71.gif"/><img src="/img/maps/52,71.gif"/><img src="/img/maps/53,71.gif"/><img src="/img/maps/54,71.gif"/><img src="/img/maps/55,71.gif"/><img src="/img/maps/56,71.gif"/><img src="/img/maps/57,71.gif"/><img src="/img/maps/58,71.gif"/><img src="/img/maps/59,71.gif"/><br/>
        <img src="/img/maps/44,72.gif"/><img src="/img/maps/45,72.gif"/><img src="/img/maps/46,72.gif"/><img src="/img/maps/47,72.gif"/><img src="/img/maps/48,72.gif"/><img src="/img/maps/49,72.gif"/><img src="/img/maps/50,72.gif"/><img src="/img/maps/51,72.gif"/><img src="/img/maps/52,72.gif"/><img src="/img/maps/53,72.gif"/><img src="/img/maps/54,72.gif"/><img src="/img/maps/55,72.gif"/><img src="/img/maps/56,72.gif"/><img src="/img/maps/57,72.gif"/><img src="/img/maps/58,72.gif"/><img src="/img/maps/rload.gif"/>
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
        title: 'Long Library - Castlevania: Symphony of the Night'
      }
    }
  }
</script>