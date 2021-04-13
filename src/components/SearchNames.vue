<template>
    <div>
        <input type="text" :input="name" @input="handleChangeName($event.target.value)">
    </div>
   <div>
       Всего <strong>{{names.length}}</strong>, совпадений <strong>{{getFilteredNames.length}}</strong>
   </div>
    <div
        v-for="(name, index) in getFilteredNames"
        :key="index"
    >
        {{name}}
    </div>

</template>

<script>
export default {
    name: "SearchNames",
    data() {
        return {
            name: '',
            names: ['Влад', 'Егор', 'Федор', 'Дмитрий', 'Иван'],
            matches: 0,
        }
    },
    methods: {
        handleChangeName(value) {
            this.name = value
        }
    },
    computed: {
        getFilteredNames() {
            return this.names.filter(name => name.toLowerCase().includes(this.name.toLowerCase()))
        }
    }
}
</script>

<style scoped>

</style>
