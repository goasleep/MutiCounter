<template>
    <div>
        <Counter v-for="n in number" v-bind:key="n" @counterValue = "countSum"></Counter>
    </div>
</template>

<script>
import Couter from './components/Counter.vue';
    export default {
        name: "CounterGroup",
        components: {
            Counter,
        },
        props: {
            number: {
                type: Number,
            },
        },
        data() {
            return {
                countSum: 0
            }
        },
        methods: {
            countSum(number) {
                countSum += number
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>