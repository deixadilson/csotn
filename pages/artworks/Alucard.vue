<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/artworks/">Artworks</NuxtLink> &raquo;
        Alucard
      </div>
      <Header/>
      <h2>Alucard</h2>
      <hr/>
      <main>
        <div>
          <div class="previous"></div>
          <div class="next"><NuxtLink to="/artworks/Alucard-2">Next &raquo;</NuxtLink></div>
        </div>
        <img src="/img/artworks/alucard.jpg"/>
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
        title: 'Alucard Artwork - Castlevania: Symphony of the Night'
      }
    }
  }
</script>