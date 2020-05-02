<template>
  <div id="app">
    <Dropdown/>
  </div>
</template>

<script>
import Dropdown from "./components/Dropdown.vue"


export default {
  name: 'App',
  components: {
    Dropdown
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700&display=swap');
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  font-family: 'Lato', sans-serif;
  background-color: #EDF2F7;
}
</style>
