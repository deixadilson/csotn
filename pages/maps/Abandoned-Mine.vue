<template>
  <div class="wrapper">
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/maps">Maps</NuxtLink> &raquo;
        Abandoned Mine
      </div>
      <Header/>
      <h2>Abandoned Mine</h2>
      <hr/>
      <main>
        <img src="/img/maps/27,89.gif"/><img src="/img/maps/rload.gif"/><br/>
        <img src="/img/maps/27,90.gif"/><br/>
        <img src="/img/maps/27,91.gif"/><img src="/img/maps/28,91.gif"/><img src="/img/maps/29,91.gif"/><img src="/img/maps/30,91.gif"/><img src="/img/maps/31,91.gif"/><img src="/img/maps/32,91.gif"/><img src="/img/maps/33,91.gif"/><img src="/img/maps/34,91.gif"/><img src="/img/maps/35,91.gif"/><img src="/img/maps/36,91.gif"/><img src="/img/maps/37,91.gif"/><br/>
        <img src="/img/maps/27,92.gif"/><img src="/img/maps/lsave.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/32,92.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/36,92.gif"/><img src="/img/maps/37,92.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/32,93.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/32,94.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/29,95.gif"/><img src="/img/maps/30,95.gif"/><img src="/img/maps/31,95.gif"/><img src="/img/maps/32,95.gif"/><img src="/img/maps/33,95.gif"/><img src="/img/maps/rload.gif"/><img src="/img/maps/35,95.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/32,96.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/32,97.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/32,98.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/31,99.gif"/><img src="/img/maps/32,99.gif"/><img src="/img/maps/33,99.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/rload.gif"/><img src="/img/maps/33,100.gif"/><br/>
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
        title: 'Abandoned Mine - Castlevania: Symphony of the Night'
      }
    }
  }
</script>