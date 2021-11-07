<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        Maps
      </div>
      <Header/>
      <h2>Maps</h2>
      <hr/>
      <main>
      <div style="text-align: center;">
        This is the map showing all the explorable rooms.<br/>
        <img src="/img/map.gif" width="514" onclick="map(event)" alt="map"/><br/>
        Legend:<br/>
        <font color="#00bbff">Common Rooms</font> | 
        <font color="#dddddd">Secret Rooms</font> | 
        <font color="#00ff00">CD Load Rooms</font> | 
        <font color="#ffcc00">Teleport Pads</font> | 
        <font color="#ff0000">Save Points</font>
        <!--<form action="">
          <select onchange="window.location=this.options[this.selectedIndex].value" style="margin: 5px;">
            <option value="">View Full Sized Map</option>
            <option value="Entrance">Entrance</option>
            <option value="Alchemy-Laboratory">Alchemy Laboratory</option>
            <option value="Marble-Gallery">Marble Gallery</option>
            <option value="Outer-Wall">Outer Wall</option>
            <option value="Long-Library">Long Library</option>
            <option value="Clock-Tower">Clock Tower</option>
            <option value="Royal-Chapel">Royal Chapel</option>
            <option value="Castle-Keep">Castle Keep</option>
            <option value="Colosseum">Colosseum</option>
            <option value="Olrox's-Quarters">Olrox's Quarters</option>
            <option value="Underground-Caverns">Underground Caverns</option>
            <option value="Abandoned-Mine">Abandoned Mine</option>
            <option value="Catacombs">Catacombs</option>
            <option value="Regular-Castle">Full Regular Castle</option>
          </select>
        </form>-->
      </div>
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
        title: 'Maps - Castlevania: Symphony of the Night'
      }
    }
  }
</script>