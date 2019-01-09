<template>
  <div v-if="this.buttonDisplay === 'today'" class="apod">
    <section>
      <h3>{{ this.apodData[0].title }}</h3>
      <p>{{ this.apodData[0].date }}</p>
      <p>{{ this.apodData[0].explanation }}</p>
      <img :src="this.apodData[0].url">
    </section>
  </div>
  <div v-else class="apod">
    <section v-for="picture in apodData">
      <h3>{{ picture.title }}</h3>
      <p>{{ picture.date }}</p>
      <p>{{ picture.explanation }}</p>
      <img :src="picture.url">
    </section>
  </div>
</template>

<script>
import apiKeys from "../../apiKeys";
import data from "../helper/apodData";

export default {
  name: "apod",
  props: ["buttonDisplay"],
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
  margin: 0 20px;
  overflow: auto;
}

section {
  align-items: center;
  border-bottom: 6px solid grey;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: 20px;
  padding: 20px;
}

h3 {
  font-size: 26px;
  margin: 10px 20%;
}

p {
  line-height: 1.8;
  margin: 20px 20%;
}

img {
  margin-top: 20px;
  max-height: 60vh;
  max-width: 80vw;
}
</style>