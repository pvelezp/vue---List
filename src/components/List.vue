<template>
    <div>
     <h1>Lista</h1>

     <div v-bind:key="item.name" v-for="item in list">
       <TodoItem v-bind:item="item" v-on:blueItem="$emit('blueish',item.name)"   />
     </div>


</div>
</template>

<script >

import TodoItem from './TodoItem.vue'

export default {
    name: 'List',
    components: {
        TodoItem
    },
    props: ['list'],

}
</script>

<style scoped>

</style>