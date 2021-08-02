<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/artworks/">Artworks</NuxtLink> &raquo;
        Librarian
      </div>
      <Header/>
      <h2>Librarian</h2>
      <hr/>
      <main>
        <div>
          <div class="previous"><NuxtLink to="/artworks/Shaft-2">&laquo; Previous</NuxtLink></div>
          <div class="next"><NuxtLink to="/artworks/Lisa">Next &raquo;</NuxtLink></div>
        </div>
        <img src="~static/img/artworks/librarian.jpg"/>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<script>
  export default { }
</script>

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