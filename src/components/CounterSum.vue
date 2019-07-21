<template>
  <div>
    <span>{{ sum }}</span>
  </div>
</template>

<script lang="ts">
export default {
  name: "CounterSum",
  props: {
    sum: {
      type: Number,
      default: 0
    }
  }
};
</script>

<style scoped>
</style>