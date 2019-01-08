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
  border: 4px solid red;
}
.title {
  color: black;
}
</style>
