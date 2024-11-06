<script>
let id = 0
export default {
  data() {
    return {
      todoName: '',
      todos: [
        { id: id++, name: 'Learn HTML' },
        { id: id++, name: 'Learn JavaScript' },
        { id: id++, name: 'Learn Vue' },
      ],
    }
  },
  methods: {
    addTodo() {
      this.todos.push({ id: id++, name: this.todoName })
      this.todoName = ''
    },
    removeTodo(todo) {
      this.todos = this.todos.filter(t => t !== todo)
    },
  },
}
</script>
<template>
  <div>
    <h1>Todo Component</h1>
    <form v-on:submit.prevent="addTodo">
      <input
        v-model="todoName"
        type="text"
        name="todoName"
        id="todoName"
        placeholder="Enter new todo.."
      />
      <button>Add Todo</button>
    </form>
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        {{ todo.name }}
        <button @click="removeTodo(todo)">X</button>
      </li>
    </ul>
  </div>
</template>
