<template>
  <div>
        <div>add todos</div>
        <input type="text" v-model="value">
        <button @click="addTodos">Add todos</button>
       <div>
            <div>My todoList</div>
            <ul>
              <li v-for="item, itemIndex in todoList":key="itemIndex">
                {{ item }}
              </li>
            </ul>
       </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      todoList: ['go to dentist', 'kill this dog'],
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
