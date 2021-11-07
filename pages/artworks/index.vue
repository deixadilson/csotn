<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        Artworks
      </div>
      <Header/>
      <h2>Artworks</h2>
      <hr/>
      <main>
        <p style="text-align: center">The official Castlevania: Symphony of the Night drawings by Ayami Kojima.</p>
        <table style="font-family: serif; font-size: 12px; text-align: center">
          <tr>
            <td><NuxtLink to="/artworks/Alucard"><img src="/img/artworks/minialucard.jpg"/><br/>Alucard</NuxtLink></td>
            <td><NuxtLink to="/artworks/Alucard-2"><img src="/img/artworks/minialucard2.jpg"/><br/>Alucard</NuxtLink></td>
            <td><NuxtLink to="/artworks/Dracula"><img src="/img/artworks/minidracula.jpg"/><br/>Dracula</NuxtLink></td>
            <td><NuxtLink to="/artworks/Dracula-2"><img src="/img/artworks/minidracula2.jpg"/><br/>Dracula</NuxtLink></td>
            <td><NuxtLink to="/artworks/Richter"><img src="/img/artworks/minirichter.jpg"/><br/>Richter Belmont</NuxtLink></td>
          </tr>
          <tr>
            <td><NuxtLink to="/artworks/Richter-2"><img src="/img/artworks/minirichter2.jpg"/><br/>Richter Belmont</NuxtLink></td>
            <td><NuxtLink to="/artworks/Maria"><img src="/img/artworks/minimaria.jpg"/><br/>Maria Renard</NuxtLink></td>
            <td><NuxtLink to="/artworks/Maria-2"><img src="/img/artworks/minimaria2.jpg"/><br/>Maria Renard</NuxtLink></td>
            <td><NuxtLink to="/artworks/Evil-Richter"><img src="/img/artworks/minievilrichter.jpg"/><br/>Evil Richter</NuxtLink></td>
            <td><NuxtLink to="/artworks/Evil-Richter-2"><img src="/img/artworks/minievilrichter2.jpg"/><br/>Evil Richter</NuxtLink></td>
          </tr>
          <tr>
            <td><NuxtLink to="/artworks/Shaft"><img src="/img/artworks/minishaft.jpg"/><br/>Shaft</NuxtLink></td>
            <td><NuxtLink to="/artworks/Shaft-2"><img src="/img/artworks/minishaft2.jpg"/><br/>Shaft</NuxtLink></td>
            <td><NuxtLink to="/artworks/Librarian"><img src="/img/artworks/minilibrarian.jpg"/><br/>Librarian</NuxtLink></td>
            <td><NuxtLink to="/artworks/Lisa"><img src="/img/artworks/minilisa.jpg"/><br/>Lisa</NuxtLink></td>
            <td><NuxtLink to="/artworks/Death"><img src="/img/artworks/minideath.jpg"/><br/>Death</NuxtLink></td>
          </tr>
          <tr>
            <td><NuxtLink to="/artworks/Succubus"><img src="/img/artworks/minisuccubus.jpg"/><br/>Succubus</NuxtLink></td>
            <td><NuxtLink to="/artworks/Ferryman"><img src="/img/artworks/miniferryman.jpg"/><br/>Ferryman</NuxtLink></td>
            <td><NuxtLink to="/artworks/Equips"><img src="/img/artworks/miniequips.jpg"/><br/>Equips</NuxtLink></td>
            <td><NuxtLink to="/artworks/Morphs"><img src="/img/artworks/minimorphs.jpg"/><br/>Morphs</NuxtLink></td>
            <td><NuxtLink to="/artworks/Spell"><img src="/img/artworks/minispell.jpg"/><br/>Spell</NuxtLink></td>
          </tr>
          <tr>
            <td><NuxtLink to="/artworks/Heal"><img src="/img/artworks/miniheal.jpg"/><br/>Heal</NuxtLink></td>
            <td colspan="3"><NuxtLink to="/artworks/Artwork"><img src="/img/artworks/miniartwork.jpg"/><br/>Artwork</NuxtLink></td>
            <td><NuxtLink to="/artworks/Artwork-2"><img src="/img/artworks/miniartwork2.jpg"/><br/>Artwork</NuxtLink></td>
          </tr>
        </table>
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
        title: 'Artworks - Castlevania: Symphony of the Night'
      }
    }
  }
</script>