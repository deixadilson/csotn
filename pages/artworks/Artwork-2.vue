<template>
  <div class="wrapper">
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/artworks/">Artworks</NuxtLink> &raquo;
        Artwork 2
      </div>
      <Header/>
      <h2>Artwork 2</h2>
      <hr/>
      <main>
        <div>
          <div class="previous"><NuxtLink to="/artworks/Artwork">&laquo; Previous</NuxtLink></div>
          <div class="next"></div>
        </div>
        <img src="/img/artworks/artwork2.jpg"/>
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