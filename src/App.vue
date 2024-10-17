<template>
  <div>
        <div>add todos</div>
        <input type="text" v-model="value">
        <button @click="addTodos">Add todos</button>
       <div>
            <div>My todoList</div>
            <TodoList :myProps="todoList"/>
       </div>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'

export default {
  components: {
    TodoList
  },
  data() {
    return {
      todoList: ['go to dentist', 'kill this dog','Drink water'],
      value: undefined,
    };
  },
  methods: {
    addTodos() {
      this.todoList.push(this.value);
      this.value = undefined;
    },
  }
  
};
</script>
