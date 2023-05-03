<template>
  <NavBar />
  <router-view />
  <FooterBar />
</template>

<script>
import NavBar from "./components/NavBar";
import FooterBar from "./components/FooterBar";

export default {
  components: {
    NavBar,
    FooterBar,
  },
};
</script>

<style>
* {
  margin: 0px;
  padding: 0px;
}
:root {
  --primary-color: #8a817c;
  --secondary-color: #bcb8b1;
  --tertiary-color: #e0afa0;
  --background-primary: #f4f3ee;
  --background-secondary: #463f3a;
}
#app {
  background-color: var(--background-primary);
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
