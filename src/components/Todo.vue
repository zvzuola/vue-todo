<template>
  <div>
    <add-todo v-on:add="add"></add-todo>
    <todo-item :key="todo.id" v-for="(todo, index) in todos" :todo="todo" v-on:remove="() => remove(index)">
      <div>children</div>
    </todo-item>
  </div>
</template>

<script>
import TodoItem from '@/components/TodoItem';
import AddTodo from '@/components/AddTodo';

export default {
  name: 'todo',
  data() {
    return {
      todos: [],
    };
  },
  methods: {
    add(text) {
      this.todos.push({
        id: Math.random(),
        text,
      });
    },
    remove(index) {
      this.todos.splice(index, 1);
    },
  },
  components: {
    AddTodo,
    TodoItem,
  },
};
</script>

