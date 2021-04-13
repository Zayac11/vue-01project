<template>
    <div id="app">
        <MyComponent />
        <Counter />
    </div>
</template>

<script>
import MyComponent from './components/MyComponent.vue'
import Counter from './components/Counter.vue'

export default {
    name: 'App',
    components: {
        MyComponent,
        Counter,
    }
}
</script>

<style>

</style>
