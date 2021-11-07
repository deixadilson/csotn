<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        <NuxtLink to="/enemies">Enemies</NuxtLink> &raquo;
        {{ enemy.Name }}
      </div>
      <Header/>
      <h2>{{ enemy.Name }}</h2>
      <hr/>
      <main>
        <div style="display: flex; align-items: center">
          <div style="width: 20px"><NuxtLink v-if="previous" :to="`/enemies/${previous.Name.replace(/ /g,'-')}`"><img src="/img/goleft.gif" alt="Previous" title="Previous"/></NuxtLink></div>
            <nuxt-child :enemy="enemy" :key="enemy.ID"></nuxt-child>
          <div><NuxtLink v-if="next" :to="`/enemies/${next.Name.replace(/ /g,'-')}`"><img src="/img/goright.gif" alt="Next" title="Next"/></NuxtLink></div>
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
        title: `${this.enemy.Name} - Castlevania: Symphony of the Night`
      }
    },
    computed: {
      enemy() {
        return this.$store.getters.enemy(this.$route.params.enemy);
      },
      previous() {
        return this.$store.getters.previous(this.enemy.ID);
      },
      next() {
        return this.$store.getters.next(this.enemy.ID);
      },
    }
  }
</script>
