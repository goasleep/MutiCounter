<template>
    <div>
        <button>-</button>
        <span>{{value}}</span>
        <button>+</button>
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
        add() {
           this.value++; 
           this.$emit("counterValue",1)
        },
        delete(){
           this.value--;
           this.$emit("counterValue",-1)
        }
    },
}
</script>

