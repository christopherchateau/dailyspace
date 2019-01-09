<template>
  <div class="daily-space-title">
    <h1 class="title">daily<img class="ufo-img" src="../images/ufo.png">space</h1>
  </div>
</template>

<script>
export default {
  name: "daily-space-title"
};
</script>

<style scoped>
.daily-space-title {
  background: black;
  margin: 20px;
  text-align: center;
}

.title {
  bottom: 18px;
  color: white;
  font-family: "Gloria Hallelujah", cursive;
  font-size: 64px;
  position: relative;
}

.ufo-img {
  height: 80px;
  margin: 0 30px;
  position: relative;
  top: 20px;
}
</style>
