<template>
  <div>
        <div>add todos</div>
        <input type="text" v-model="value">
        <button @click="addTodos">Add todos</button>
       <div>
            <div>My todoList</div>
            <TodoList :myProps="todoList" @removeToDo="removeElements"/>
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
      todoList: ['go to dentist', 'Drink water'],
      value: undefined,
    };
  },
  methods: {
    addTodos() {
      this.todoList.push(this.value);
      this.value = undefined;
    },
    removeElements(toDo) {
      this.todoList.splice(this.todoList.indexOf(toDo), 1)
    }
  }
  
};
</script>
