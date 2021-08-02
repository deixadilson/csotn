<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        Search Results
      </div>
      <Header/>
      <h2>Search Results</h2>
      <hr/>
      <main>
        <div id="cse-search-results"></div>
        <script type="text/javascript">
        var googleSearchIframeName = "cse-search-results";
        var googleSearchFormName = "cse-search-box";
        var googleSearchFrameWidth = 800;
        var googleSearchDomain = "www.google.com.br";
        var googleSearchPath = "/cse";
        </script>
        <script type="text/javascript" src="http://www.google.com/afsonline/show_afs_search.js"></script>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<script>
  export default {}
</script>