<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/videos">Videos</NuxtLink> &raquo;
        Godly Alucard
      </div>
      <Header/>
      <h2>Godly Alucard</h2>
      <hr/>
      <main>
        <iframe width="734" height="500" src="https://www.youtube.com/embed/Z4oXkBXVflY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<script>
  export default {
    head() {
      return {
        title: 'Godly Alucard - Castlevania: Symphony of the Night'
      }
    }
  }
</script>