<template>
  <div class="app">
    <DailySpaceTitle/>
    <APOD v-bind:buttonDisplay="buttonDisplay"/>
    <div class="footer">
      <button class="footer-btn" v-on:click="handleClick">{{ buttonDisplay }}</button>
    </div>
  </div>
</template>

<script>
import DailySpaceTitle from "./components/DailySpaceTitle.vue";
import APOD from "./components/APOD.vue";

export default {
  name: "app",
  props: {
    appButtonDisplay: "asd"
  },
  data() {
    return {
      buttonDisplay: "this month"
    };
  },
  methods: {
    handleClick: function() {
      this.buttonDisplay === "today"
        ? (this.buttonDisplay = "this month")
        : (this.buttonDisplay = "today");
    }
  },

  components: {
    DailySpaceTitle,
    APOD
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Rubik");
@import url('https://fonts.googleapis.com/css?family=Gloria+Hallelujah');

* {
  font-family: "Rubik", sans-serif;
  margin: 0;
}

.app {
  background: silver;
  display: grid;
  grid-auto-rows: 150px 1fr 150px;
  height: 100vh;
}

.footer {
  align-items: center;
  background: black;
  display: flex;
  justify-content: center;
  margin: 20px;
}

.footer-btn {
  background: grey;
  border: 4px solid white;
  color: white;
  cursor: pointer;
  font-family: "Gloria Hallelujah", cursive;
  font-size: 32px;
  padding: 0 30px;
  transition: all 0.4s ease-in-out;
}

.footer-btn:hover {
  background: white;
  color: black;
  transition: all 0.4s ease-in-out;
}
</style>