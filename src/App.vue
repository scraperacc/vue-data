<template>
  <div id="app">
    <ExampleOfIncorrectUseData />
    <ExampleOfCorrectUseData />
  </div>
</template>

<script>
import ExampleOfIncorrectUseData from "./components/ExampleOfIncorrectDefineData";
import ExampleOfCorrectUseData from "./components/ExampleOfCorrectDefineData";

export default {
  name: 'App',

  components: {
    ExampleOfCorrectUseData,
    ExampleOfIncorrectUseData

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
