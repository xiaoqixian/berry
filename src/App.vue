<template>
  <banner />
  <main-window />
</template>

<script>
import Banner from './components/Banner.vue'
import MainWindow from './components/MainWindow.vue'

export default {
  name: "App",
  components: {
    Banner,
    MainWindow
  }
}
</script>

<style>
body {
  background-color: #fefefe;
}

html, body, #app {
  display: flex;
  width: 100%;
  height: 100%;
  flex-direction: column;
  padding: 0px;
  margin: 0px;
}


</style>
