<template>
  <div id="app">
        <ol>
            <todo-item v-for = "item in groceryList" v-bind:todo="item" v-bind:key="item.id">

            </todo-item>
        </ol>
  </div>
</template>

<script>
import TodoItem from './components/TodoItem.vue'

export default {
  name: 'app',
  data(){
    return{
      groceryList: [
      {    
          id: 0,
          text: '🧀️'
      },{
          id: 1,
          text: '👃'
      },{
          id: 2,
          text: '🚚'
      }]
    }
  },
  components: {
    TodoItem
  }
}
</script>