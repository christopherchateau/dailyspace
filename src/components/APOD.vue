<template>
  <div class="apod">
    <h3>apod</h3>
    
  </div>
</template>

<script>
import apiKeys from "../../apiKeys";
import data from "../helper/apodData";

export default {
  name: "apod",

  async mounted() {
    // const response = await fetch(
    //   `https://api.nasa.gov/planetary/apod?api_key=${apiKeys.private}`
    // );
    // const data = await response.json();

    this.apodData = data;
  },

  data() {
    return {
      apodData: []
    };
  }
};
</script>

<style scoped>
.apod {
  background: black;
  color: white;
  margin: 20px;
}
</style>