<template>
  <div>
    <input v-model.number="count" />
    <CounterGroup :number="count" @calculateSum="getCountSum"></CounterGroup>
    <CounterSum :sum="countSum "></CounterSum>
  </div>
</template>

<script lang="ts">
import CounterGroup from "@/components/CounterGroup.vue";
import CounterSum from "@/components/CounterSum.vue";

export default {
  name: "MutiCounter",
  components: {
    CounterSum,
    CounterGroup
  },
  data() {
    return {
      count: 0,
      countSum: 0
    };
  },
  methods: {
    getCountSum(countSum) {
      this.countSum = countSum;
    },
    reset() {
      this.countSum = 0;
    }
  }
};
</script>

<style scoped>
</style>