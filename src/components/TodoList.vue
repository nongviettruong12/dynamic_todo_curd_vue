<template>
        <ul>
              <Todo v-for="item, itemIndex in myProps " :key="itemIndex" :toDo="item" />
            </ul>
</template>
<script>
import Todo from './Todo.vue'
export default {
  components: {
    Todo
  },
  props: {
    myProps:{
      type: Array,
      default: () =>[

      ]
    }
  }
}
</script>