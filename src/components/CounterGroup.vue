<template>
  <div>
    <Counter v-for="n in number" v-bind:key="n" @counterValue="calculate"></Counter>
  </div>
</template>

<script>
import Counter from "@/components/Counter.vue";
export default {
  name: "CounterGroup",
  components: {
    Counter
  },
  props: {
    number: {
      type: Number,
      default: 1
    }
  },
  data() {
    return {
      countSum: 0
    };
  },
  methods: {
    calculate(number) {
      this.countSum += number;
      this.$emit("calculateSum", this.countSum);
    }
  }
};
</script>

<style lang="scss" scoped>
</style>