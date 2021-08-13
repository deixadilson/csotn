<template>
  <div class="wrapper">
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/artworks/">Artworks</NuxtLink> &raquo;
        Artwork
      </div>
      <Header/>
      <h2>Artwork</h2>
      <hr/>
      <main>
        <div>
          <div class="previous"><NuxtLink to="/artworks/Heal">&laquo; Previous</NuxtLink></div>
          <div class="next"><NuxtLink to="/artworks/Artwork-2">Next &raquo;</NuxtLink></div>
        </div>
        <img src="/img/artworks/artwork.jpg"/>
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