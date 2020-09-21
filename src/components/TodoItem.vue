<template>
    <div 
    class="item"
    v-on:click="blueish"
   >
   <p
    class="todo-item" v-bind:class="{'is-clicked':item.clicked}"
   >{{item.name}} tiene {{item.length}} productos - su mayor producto es {{item.products[0].name}} y su precio: {{item.products[0].price}} </p>
    </div>
</template>

<script >
   export default {
       name: "TodoItem",
       props:["item"],
       methods: {
           blueish() {
              this.item.clicked = !this.item.clicked
           }
       }
       } 
</script>

<style scoped>
.item {
    cursor: pointer;
}

.todo-item {
    background: #f4f4f4;
    padding:10px;
    border-bottom: 1px #ccc dotted;
    margin-bottom: 6px;
    box-shadow: 1px 2px 0px 0px rgba(0,0,0,0.2)
}

.is-clicked {
    color: blue;
    }
</style>