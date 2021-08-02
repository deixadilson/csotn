<template>
  <aside>
    <NuxtLink to="/"><img src="~static/img/god.jpg" alt="Game Oracle Deixadilson"/></NuxtLink>
    <div class="cse-branding-bottom" style="background-color: #000; color: #fff;">
      <div class="cse-branding-form">
        <form action="/search" id="cse-search-box">
          <div>
            <input type="hidden" name="cx" value="partner-pub-8005806211984814:j70qnt4xisc"/>
            <input type="hidden" name="cof" value="FORID:10"/>
            <input type="hidden" name="ie" value="ISO-8859-1"/>
            <input type="text" name="q" size="16"/><input type="submit" name="sa" value="Search"/>
          </div>
        </form>
      </div>
      <div class="cse-branding-logo">
          <img src="http://www.google.com/images/poweredby_transparent/poweredby_000000.gif" alt="Google"/> Custom Search
      </div>
    </div>
    <nav>
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/story">Story</NuxtLink>
      <NuxtLink to="/system">System</NuxtLink>
      <NuxtLink to="/walkthrough">Walkthrough</NuxtLink>
      <NuxtLink to="/maps/">Maps</NuxtLink>
      <NuxtLink to="/enemies/">Enemies</NuxtLink>
      <NuxtLink to="/items/">Items</NuxtLink>
      <NuxtLink to="/secrets">Secrets</NuxtLink>
      <NuxtLink to="/oddities">Oddities</NuxtLink>
      <NuxtLink to="/videos/">Videos</NuxtLink>
      <NuxtLink to="/artworks">Artworks</NuxtLink>
    </nav>
    <a href="?lang=br"><img src="~static/img/br.png" alt="Português do Brasil" title="Português do Brasil"/></a>
    <a href="?lang=www"><img src="~static/img/us.png" alt="English" title="English"/></a>
    <h3>Online:</b> </h3>
    <h3>Donations:</h3>
    <form action="https://www.paypal.com/cgi-bin/webscr" method="post">
      <input type="hidden" name="cmd" value="_s-xclick"/>
      <input type="hidden" name="hosted_button_id" value="4662790"/>
      <input type="image" src="~static/img/donate.png" name="submit" alt="Contribua!"/>
    </form>
  </aside>
</template>

<script>
  export default {}
</script>

<style scoped>
  .cse-branding-logo img {
    vertical-align: sub;
  }
</style>