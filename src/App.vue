<template>
  <div id="app">
    <Header />
    <Main />
  </div>
</template>

<script>

import Main from './components/Main';
import Header from './components/Header';

export default {
  name: 'App',
  components: {
    Header,
    Main,
  }
}
</script>

<style lang="scss">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
</style>
