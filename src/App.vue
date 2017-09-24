<template>
  <div id="app">
    <app-header offset="56"></app-header>
    <main>
      <router-view></router-view>
    </main>
  </div>
</template>

<script>

import appHeader from './components/AppHeader';

export default {
  name: 'app',
  components: {
    appHeader,
  },
};
</script>

<style>
body {
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

main {
  text-align: center;
  margin-top: 56px;
}
</style>
