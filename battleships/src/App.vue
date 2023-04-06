<template>
  <HomePage />
  <BuildLayout />
</template>

<script>
import HomePage from './components/HomePage.vue';
import BuildLayout from "@/components/BuildLayout";
import DataLayout from './data/DataLayout';



export default {
  name: 'App',
  components: {
    BuildLayout,
    HomePage
  },
  data(){
    return{
      DataLayout
    }
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
