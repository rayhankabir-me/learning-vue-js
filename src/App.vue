<script>
import ButtonCounter from './components/ButtonCounter.vue'
import ColorComponent from './components/ColorComponent.vue'

export default {
  components: {
    ButtonCounter,
    ColorComponent,
  },
  data() {
    return {
      message: 'hello world',
      status: 'pending',
      tasks: ['Task One', 'Task Two', 'Task Three'],
    }
  },
  methods: {
    toggleStatus() {
      if (this.status === 'active') {
        this.status = 'pending'
      } else if (this.status === 'pending') {
        this.status = 'inactive'
      } else {
        this.status = 'inactive'
      }
    },
  },
}
</script>
<template>
  <h1>{{ message }}</h1>
  <p v-if="status === 'active'">user is active</p>
  <p v-else-if="status === 'pending'">user is pending</p>
  <p v-else>user is inactive</p>
  <h3>Tasks Lists:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>

  <button v-on:click="toggleStatus">Toggle Status</button>
  <br />
  <hr />
  <ButtonCounter />

  <h1>color component experiment</h1>
  <ColorComponent />
</template>
