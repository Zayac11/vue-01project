<template>
    <div class="container">
        <div>
            Введите количество продуктов:
        </div>
        <button v-on:click="decrementFunction">-</button>
        <input type="number" @input="numberInput($event.target.value)" v-model="count">
        <button v-on:click="incrementFunction">+</button>

    </div>
</template>

<script>
export default {
    name: 'Counter',
    data() {
        return {
            count: 0,
        }
    },
    methods: {
        numberInput(value) {
            this.count = value
        },
        incrementFunction() {
            if(this.count<10) this.count++
        },
        decrementFunction() {
            if(this.count>0) this.count--
        },
    }
}
</script>

<style>
    /*.container {*/
    /*    width: 1200px;*/
    /*    margin: 20px auto;*/
    /*}*/
</style>
