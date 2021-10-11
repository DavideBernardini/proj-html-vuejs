<template>
  <div id="app">
    <Header :sections="sections"/>
    <Main/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data() {
    return {
      sections: ['home', 'services', 'about', 'projects', 'results']
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

</style>
