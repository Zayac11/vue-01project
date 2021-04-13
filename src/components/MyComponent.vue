<template>
    <div class="container">
        <div>
            <input type="text" @input="emailInput($event.target.value)" :input="name">
        </div>
        <div>
            <input type="password" v-on:input="passwordInput" :input="password">
        </div>
        <div>
            <div>{{name}}</div>
            <div>{{password}}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MyComponent',
    data() {
        return {
            name: '',
            password: '',
        }
    },
    methods: {
        emailInput(value) {
            this.name = value
        },
        passwordInput(e) {
            this.password = e.target.value
        },
    }
}
</script>

<style>
    .container {
        width: 1200px;
        margin: 20px auto;
    }
</style>
