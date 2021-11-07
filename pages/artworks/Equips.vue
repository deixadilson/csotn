<template>
  <div class="wrapper">
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/artworks/">Artworks</NuxtLink> &raquo;
        Equips
      </div>
      <Header/>
      <h2>Equips</h2>
      <hr/>
      <main>
        <div>
          <div class="previous"><NuxtLink to="/artworks/Ferryman">&laquo; Previous</NuxtLink></div>
          <div class="next"><NuxtLink to="/artworks/Morphs">Next &raquo;</NuxtLink></div>
        </div>
        <img src="/img/artworks/equips.jpg"/>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<style scoped>
  main {
    display: flex;
    flex-direction: column;
  }
  main img {
    margin: 0 auto;
    width: 100%;
  }
  .previous {
    float: left;
  }
  .next {
    float: right;
  }
</style>

<script>
  export default {
    head() {
      return {
        title: 'Equips Artwork - Castlevania: Symphony of the Night'
      }
    }
  }
</script>