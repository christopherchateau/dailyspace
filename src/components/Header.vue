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
  background: rgb(215, 215, 215);
  display: grid;
  margin: 20px;
  justify-content: center;
}
.title {
  color: white;
  color: black;
  font-size: 42px;
}
</style>
