<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/videos">Videos</NuxtLink> &raquo;
        Richter's Dark Spiked Room
      </div>
      <Header/>
      <h2>Richter's Dark Spiked Room</h2>
      <hr/>
      <main>
        <iframe width="734" height="500" src="https://www.youtube.com/embed/m3DHz-GYedo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<script>
  export default {}
</script>