<template>
  <div class="wrapper">
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/maps">Maps</NuxtLink> &raquo;
        Outer Wall
      </div>
      <Header/>
      <h2>Outer Wall</h2>
      <hr/>
      <main>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/rsave.gif"/><img src="/img/maps/61,64.gif"/><img src="/img/maps/62,76.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/rload.gif"/><img src="/img/maps/61,65.gif"/><img src="/img/maps/62,65.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/60,66.gif"/><img src="/img/maps/61,66.gif"/><img src="/img/maps/62,66.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/60,67.gif"/><img src="/img/maps/61,67.gif"/><img src="/img/maps/62,67.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/59,68.gif"/><img src="/img/maps/60,68.gif"/><img src="/img/maps/61,68.gif"/><img src="/img/maps/62,68.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/60,69.gif"/><img src="/img/maps/61,69.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/60,70.gif"/><img src="/img/maps/61,73.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/60,71.gif"/><img src="/img/maps/61,71.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/rload.gif"/><img src="/img/maps/60,72.gif"/><img src="/img/maps/61,72.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/60,73.gif"/><img src="/img/maps/61,73.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/56,74.gif"/><img src="/img/maps/57,74.gif"/><img src="/img/maps/58,74.gif"/><img src="/img/maps/59,74.gif"/><img src="/img/maps/60,74.gif"/><img src="/img/maps/61,74.gif"/><br/>
        <img src="/img/maps/rsave.gif"/><img src="/img/maps/56,75.gif"/><img src="/img/maps/57,75.gif"/><img src="/img/maps/58,75.gif"/><img src="/img/maps/59,75.gif"/><img src="/img/maps/60,75.gif"/><img src="/img/maps/61,75.gif"/><img src="/img/maps/62,75.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/rload.gif"/><img src="/img/maps/61,76.gif"/><img src="/img/maps/62,76.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/59,77.gif"/><img src="/img/maps/60,77.gif"/><img src="/img/maps/61,77.gif"/><img src="/img/maps/62,77.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/59,78.gif"/><img src="/img/maps/60,78.gif"/><img src="/img/maps/61,78.gif"/><img src="/img/maps/62,78.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/60,79.gif"/><img src="/img/maps/61,79.gif"/><img src="/img/maps/62,79.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/60,80.gif"/><img src="/img/maps/61,80.gif"/><br/>
        <img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/blank.gif"/><img src="/img/maps/60,81.gif"/><img src="/img/maps/61,81.gif"/>
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
        title: 'Outer Wall - Castlevania: Symphony of the Night'
      }
    }
  }
</script>