<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        Items
      </div>
      <Header/>
      <h2>Items</h2>
      <hr/>
      <main>
        <p>The full list of items and relics.</p>
        <Inventory/>
        <div id="stats"></div>
        <div id="info"></div>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<style scoped>
  p{
    text-align: center;
  }
  #stats{
    width: 300px;
    height: 400px;
    padding: 4px;
    border-style: solid;
    border-left: 0;
    float: left;
  }
  #info{
    width: 600px;
    height: 65px;
    border-style: solid;
    border-top: 0;
    padding-right: 19px;
    margin-left: 54px;
    clear: left;
  }
  #stats, #info{
    background: linear-gradient(#020223, #1d1d5c);
  }
</style>