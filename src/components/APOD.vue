<template>
  <div class="apod">
    <section v-for="picture in apodData">
      <h3>{{ picture.title }}</h3>
      <p>{{ picture.date }}</p>
      <p>{{ picture.explanation }}</p>
      <img class="image" :src="picture.url">
    </section>
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
  overflow: auto;
}

section {
  align-items: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 20px;
}

h3 {
  font-size: 26px;
}

.image {
  max-width: 90vw;
}
</style>