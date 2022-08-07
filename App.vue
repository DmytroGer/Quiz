<template>
  <div id="app">
    <Quiz />
    <router-view />
  </div>
</template>

<script>
import Quiz from './components/Quiz.vue'
import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap-vue/dist/bootstrap-vue.css';
export default {
  name: 'App',
  components: {
    Quiz
  }
}
};
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
@import './styles/main.scss';
@font-face {
  font-family: 'PatrickHand';
  src: url('./assets/font/PatrickHand-Regular.ttf');
  src: local('PatrickHand Regular'), local('PatrickHand-Regular'),
    url('./assets/font/PatrickHand-Regular.ttf') format('opentype');
  // font-weight: normal;
  // font-style: normal;
}
</style>
