<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        Videos
      </div>
      <Header/>
      <h2>Videos</h2>
      <hr/>
      <main>
        <p>Here you'll find my Castlevania: Symphony of the Night YouTube videos.</p>
        <table>
          <tr><td><NuxtLink to="/videos/85HP"><img src="~static/img/videos/85hp.jpg" alt="How to start with 85 HP"/></NuxtLink></td><td><b>How to start with 85 HP</b><br/>Defeating Dracula under 1 minute, without Sub-Weapon to start the game with 85 HP.<br/>Duration: 01:02</td></tr>
          <tr><td><NuxtLink to="/videos/Prologue-Glitch"><img src="~static/img/videos/prologue-glitch.jpg" alt="Richter's Prologue Glitch"/></NuxtLink></td><td><b>Richter's Prologue Glitch</b><br/>Making Richter get off screen and hiding under Dracula's cloak at the start of the game.<br/>Duration: 01:11</td></tr>
          <tr><td><NuxtLink to="/videos/Spiked-Room"><img src="~static/img/videos/spiked-room.jpg" alt="Richter's Dark Spiked Room"/></NuxtLink></td><td><b>Richter's Dark Spiked Room</b><br/>How to pass by the Catacomb's Dark Spiked Room as Richter Belmont.<br/>Duration: 1:43</td></tr>
          <tr><td><NuxtLink to="/videos/Richter-Speedrun"><img src="~static/img/videos/richter-speedrun.jpg" alt="Richter Speedrun"/></NuxtLink></td><td><b>Richter Speedrun</b><br/>Speedrun as Richter Belmont Beating the game in 6:18 minutes from the game start till last hit on Shaft (I think the sound is a little loud...).<br/>Duration: 6:28</td></tr>
          <tr><td><NuxtLink to="/videos/Godly-Alucard"><img src="~static/img/videos/godly-alucard.jpg" alt="Godly Alucard"/></NuxtLink></td><td><b>Godly Alucard</b><br/>Alucard with maxed status, 999 Attack and 100 Defense showing who rules that Castle!<br/>Duration: 6:34</td></tr>
        </table>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<script>
  export default {}
</script>