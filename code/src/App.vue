<template>
  <div id="app">
    <Header/>
    <Information/>
    <img id="background" src="@/assets/background.jpeg">
  </div>
</template>

<script>

import Header from "./components/Header";
import Information from "./components/Information";

export default {
  name: 'App',
  components: {
    Information,
    Header
  }
}
</script>

<style>
body {
  display: flex;
  height: 100vh;
  width: 100vw;
  margin: 0;
  padding: 0;
  margin: auto;
  justify-content: center;
  min-height: 660px;

}

#background {
  object-fit: cover;
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  z-index: -1;
  opacity: 0.20;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  align-self: center;
}
</style>
