<template>
  <div class="header">
    <h1 class="title">{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: "header",
  data() {
    return {
      title: "daily space"
    };
  }
};
</script>

<style scoped>
.header {
  align-items: center;
  background: black;
  display: grid;
  margin: 20px;
  justify-content: center;
}
.title {
  color: white;
  font-size: 42px;
}
</style>
