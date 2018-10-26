<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from '@/components/Header.vue';

export default {
  name: 'app',
  components: {
    Header,
  },
}
</script>

<style lang="scss">
  @import "~/_variables.scss";
  @import url('https://fonts.googleapis.com/css?family=Lato:300,400,700');

  #app {
    background-color: $appBackground;
    min-height: 100vh;
    padding-bottom: 30vh;
  }
</style>
