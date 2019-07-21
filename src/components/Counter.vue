<template>
    <div>
        <button @click="decrease">-</button>
        <span>{{ value }}</span>
        <button @click="increase">+</button>
    </div>
    
</template>

<script>
export default {
    name: 'Counter',
    data() {
        return {
            value: 0
        }
    },
    methods: {
        increase() {
           this.value++; 
           this.$emit("counterValue",1)
        },
        decrease(){
           this.value--;
           this.$emit("counterValue",-1)
        }
    },
}
</script>

