<template>
  <div class="daily-space-title">
    <h1 class="title">{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: "daily-space-title",
  data() {
    return {
      title: "daily space"
    };
  }
};
</script>

<style scoped>
.daily-space-title {
  align-items: center;
  background: black;
  display: grid;
  margin: 20px;
  justify-content: center;
}
.title {
  color: white;
  font-size: 44px;
}
</style>
