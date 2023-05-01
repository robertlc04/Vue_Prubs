<template>
  <NavBar />
  <router-view />
</template>

<script>
import NavBar from "./components/NavBar";

export default {
  components: {
    NavBar,
  }
}
</script>

<style>
* {
  margin: 0px;
  padding: 0px;
}
:root {
    --primary-color: #8A817C;
    --secondary-color: #BCB8B1 ;
    --tertiary-color: #E0AFA0;
    --background-primary: #f4f3ee;
    --background-secondary: #463F3A;
}
#app {
  background-color: var(--background-primary);
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
