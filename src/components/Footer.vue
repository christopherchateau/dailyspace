<template>
  <div class="footer">
    <button v-on:click="toggleDisplay">{{ buttonDisplay }}</button>
  </div>
</template>

<script>
export default {
  name: "footer",
  props: {
    buttonDisplay: {
      type: String
    }
  },
  data() {
    return {
      buttonDisplay: 'today'
    };
  },
  methods: {
    toggleDisplay: function() {
      this.$emit('toggleDisplay', "this month")
    }
  }
};
</script>

<style scoped>
.footer {
  background: rgb(215, 215, 215);
  margin: 20px;
}
</style>