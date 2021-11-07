<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        Castlevania: Symphony of the Night
      </div>
      <Header/>
      <hr/>
      <main>
        <p>Castlevania: Symphony of the Night (SotN) is an action/adventure game developed by Konami Computer Entertainment Tokyo and published by Konami for the PlayStation in 1997. In the following year a Sega Saturn version was released in Japan. Its Japanese title is Demon Castle Dracula X: Nocturne in the Moonlight (Akumajou Dracula X: Gekka no Yasokyoku), part of the Castlevania series and direct sequel of Demon Castle Dracula X: Rondo of Blood for the NEC PC Engine/TurboGrafx 16.</p>
        <p>The story evolves around Adrian Fahrenheights Tepes, son of Count Dracula and the human Lisa, therefore, born a half-vampire. Lisa defended the humans and taught it to Adrian until she was sentenced to death by her fellows who hated Dracula. After seeing his dead mother, Adrian develops a feeling of hatred against his father who did nothing to prevent the death of Lisa and therefore changes his name to Alucard, for the will of being the opposite of his father, Dracula.</p>
        <p>Dracula in Castlevania is the Lord of the Vampires whom the Belmont clan of vampire hunters have the mission to defeat, passing from generation to generation the sacred whip, Vampire Killer. Dracula is reborn each century when the new generation of Belmonts has the duty to once again destroy him. Alucard had helped a member of the Belmont clan, Trevor Belmont, to destroy his immortal father in Castlevania III: Dracula's Curse, released on the NES, and after that he fell asleep in order to hide his vampiric powers.</p>
        <p>Castlevania: Symphony of the Night starts in 1792 when Richter Belmont completes his fate of destroying Count Dracula who had been brought back to life by the Dark Priest Shaft. But 4 years later, Richter mysteriously vanished. Feeling once again the acting of evil in his homeland, Alucard awakens from his sleep of 300 years and heads to Castlevania, Dracula's Castle, while Maria Renard enters looking for Richter, her brother in law.</p>
        <p>Unlike the previous games of the saga, Castlevania: Symphony of the Night innovates with features such as level up system, items, equipments and the ability to freely explore the scenery as the game is no longer divided into stages.</p>
        <p>The graphics and sounds has much evolved in this Playstation version. The entire scenery, the characters and enemies are full of detail. Effects of light and shadow grants a flawless look for a 2D game. The already awesome Castlevania soundtracks got even better with CD quality in the compositions of Michiru Yamane. The designer Ayami Kojima was the responsible for the excellent character design of Symphony of the Night. The game has a very impressive amount of characters and enemies sprites which gives them smooth animations in contrast to the limited movements of the previous games. The new style can be noticed in subsequent games of the saga such as Castlevania Harmony of Dissonance and Lament of Innocence.</p>
        <p>Despite not having success immediately after its release in the United States, Symphony of the Night is still present in the list of the best games of all time.</p>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<style>
  @font-face{
      font-family: sotn;
      src: url(/OldEnglish.ttf);
  }

  body{
    background: #000;
    font-family: sans-serif;
    color: #fff;
    text-align: justify;
    min-width: 992px;
  }

  h1, h2, h3, h4, h5, h6{
    font-family: 'Old English Text MT', 'sotn';
    font-weight: normal;
    text-shadow: 2px 2px 0 #000;
    text-align: center;
  }

  a, a:visited{
    font-weight: bold;
    color: #fff;
    text-decoration: none;
  }

  a:hover{
    color: #ff0;
  }

  a:active{
    color: #f00;
  }

  aside{
    width: 210px;
    color: #888;
    text-align: center;
    float: left;
  }
  
  nav{
    margin-bottom: 20px;
  }

  nav a{
    width: 200px;
    padding: 4px 0 0 15px;
    display: block;
    background: url(/img/button.gif) no-repeat;
    text-align: left;
    color: #fff;
    font: 36px 'Old English Text MT', 'sotn';
    text-shadow: 2px 2px 0 #000;
  }

  .container{
    width: 734px;
    padding: 20px;
    min-height: 933px;
    background: url(/bg.png) no-repeat fixed 200px 0px;
    line-height: 180%;
    float: left;
  }

  footer{
    text-align: center;
  }
</style>
