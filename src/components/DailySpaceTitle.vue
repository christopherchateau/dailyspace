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
  background: black;
  margin: 20px;
  text-align: center;
}
.title {
  color: white;
  font-size: 64px;
  padding-top: 12px;
}
</style>
