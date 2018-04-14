<template>
  <div id="app">
    <WordCounter />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import WordCounter from './components/WordCounter.vue';

export default Vue.extend({
  name: 'App',
  components: {
    WordCounter
  }
});
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
