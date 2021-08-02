<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        Easter Eggs
      </div>
      <Header/>
      <h2>Easter Eggs</h2>
      <hr/>
      <main>
        <center><NuxtLink to="oddities">Oddities</NuxtLink> | <NuxtLink to="easter-eggs">Easter Eggs</NuxtLink> | <NuxtLink to="bugs">Bugs</NuxtLink> | <NuxtLink to="glitches">Glitches</NuxtLink></center>
        <p>Aqui estão os Easter Eggs (Coisas curiosas feitas de propósito pelos criadores do game) catalogadas por meu amigo, <b>Jack (O' Bones) Wilker Barros</b>.</p>
        <ol>
          <li><b>Hidden audio track:</b> If you insert the Castlevania: Symphony of the Night <abbr title="Compact Disc">CD</abbr> in a <abbr title="Compact Disc">CD</abbr> player, you will notice there is an audio track and if you play it you will hear Alucard saying "As you can see, this is a playstation black disc. Track number one contains computer data, so please, don't play it. But you probably won't listen to me anyway, will you?" Then you will hear a mix of Castlevania/Gradius style song. (Gradius is a spaceship shooting game also from Konami).</li>
          <li><b>Família de morcegos:</b> Quando Alucard se transforma em morcego com o 'Bat Familiar' ativado e com level um pouco elevado, aparecem outros  morceguinhos que o seguem. Alucard pode ter até 4 morcegos o seguindo, dependendo do Level do familiar. Isto foi inspirado em pequenos globos que seguem a nave do jogo Gradius. Neste jogo quando a nave atira, todos os globos que a seguem atiram juntos. Assim acontece com os morcegos. Quando Alucard usa o <Item item="Fire of Bat"/>, todos os morcegos atiram bolas de fogo.</li>
          <li><b>Sobre o especial do <Item item="Shield rod"/> (<img src="~static/img/tras.gif" alt="Esqurda"/> <img src="~static/img/frente.gif" alt="Frente"/> + <img src="~static/img/quadrado.gif" alt="Quadrado"/> ou <img src="~static/img/circulo.gif" alt="Círculo"/>):</b> Alucard lança pequenos escudos em forma de engrenagens, também inspirados no Jogo Gradius que servem para bloquear projéteis dos inimigos. Se você fizer o especial e acertar em um inimigo de perto, contarão 2 hits com bônus no dano!</li>
          <li><b>Alucard's true form:</b> Sometimes when Alucard turns into stone he takes the shape of a huge dragon. Some fans speculates that it's the true form of Alucard as the second form of Dracula when he fights agains Richter in the prolog is his true form as himself claims to be.</li>
          <li><b>Família de gaivotas no jogo:</b> Em <NuxtLink to="maps/Outer-Wall">Outer Wall</NuxtLink>, na parte mais inferior da área, mais específicamente, embaixo da sala onde fica a luneta, você poderá ver, na primeira vez que entrar na sala, uma gaivota preparando um ninho. Se você sair e entrar na sala novamente, você poderá ver a gaivota pondo ovos, chocando-os, alimentando os filhotes enquanto eles vão crescendo até tornarem-se adultos e o ciclo recomeçar. </li>
          <li><b>A Fada senta no seu ombro:</b> Se você passar algum tempo parado com a 'Faerie Familiar' acionada, ela se senta em seu ombro. Após isso, se você se mover, se transformar ou equipar a <Item item="Axe Lord armor"/>, ela se assusta.</li>
          <li><b>Personagens de O Mágico de Oz:</b> Os famosos Personagens de O Mágico de Oz, <NuxtLink to="enemies/Lion">Leão</NuxtLink>, <NuxtLink to="enemies/Scarecrow">Espantalho</NuxtLink> e <NuxtLink to="enemies/Tin-man">Homem de lata</NuxtLink> estão presentes no jogo em Reversed Long Library</li>
        </ol>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<script>
  export default {}
</script>

<style scoped>
  li { margin-bottom: 15px; }
</style>