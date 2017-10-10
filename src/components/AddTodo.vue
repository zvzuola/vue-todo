<template>
  <div>
    <input v-model="newTodoText"/>
    <button @click="addTodo">添加todo</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodoText: '',
    };
  },
  methods: {
    addTodo() {
      this.$emit('add', this.newTodoText);
    },
  },
};
</script>

