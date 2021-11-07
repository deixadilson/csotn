<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/artworks/">Artworks</NuxtLink> &raquo;
        Maria 2
      </div>
      <Header/>
      <h2>Maria 2</h2>
      <hr/>
      <main>
        <div>
          <div class="previous"><NuxtLink to="/artworks/Maria">&laquo; Previous</NuxtLink></div>
          <div class="next"><NuxtLink to="/artworks/Evil-Richter">Next &raquo;</NuxtLink></div>
        </div>
        <img src="/img/artworks/maria2.jpg"/>
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
        title: 'Maria Artwork 2 - Castlevania: Symphony of the Night'
      }
    }
  }
</script>