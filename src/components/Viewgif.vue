<template>
  <div class="img__section">
    <img alt="" :src="catUrl" />
  </div>
</template>

<script>
export default {
  name: "Viewgif",
  props: {
    catUrl: { type: String, required: true },
  },
};
</script>

<style scoped>
.img__section {
  display: flex;
  justify-content: center;
  padding: 2em;
}
</style>