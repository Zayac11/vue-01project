<template>
    <div id="app">
<!--        <MyComponent />-->
<!--        <Counter />-->
<!--        <UserCard />-->
        <SearchNames />
    </div>
</template>

<script>
// import MyComponent from './components/MyComponent.vue'
// import Counter from './components/Counter.vue'
// import UserCard from "./components/UserCard";

import SearchNames from "./components/SearchNames";
export default {
    name: 'App',
    components: {
        SearchNames
        // MyComponent,
        // Counter,
        // UserCard,
    }
}
</script>

<style>

</style>
