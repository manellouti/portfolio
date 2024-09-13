<template>
  <div id="app">
    <CreationHeader />
    <router-view />
    <CreationFooter />
  </div>
</template>

<script>
import CreationHeader from "./components/CreationHeader.vue";
import CreationFooter from "./components/CreationFooter.vue";

export default {
  components: {
    CreationHeader,
    CreationFooter,
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
