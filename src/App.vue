<template>
  <div class="app">
    <Header/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Header,
    Main,
    Footer
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Rubik");

.app {
  display: grid;
  grid-auto-rows: 150px 1fr 150px;
  height: 100vh;
}
</style>
