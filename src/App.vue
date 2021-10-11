<template>
  <div id="app">
    <Header/>
    <Hero/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';

export default {
  name: 'App',
  components: {
    Header,
    Hero
  }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';

</style>
