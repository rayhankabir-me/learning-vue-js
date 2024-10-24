<script>
export default {
  data() {
    return {
      titleClass: 'green_title',
    }
  },
  methods: {
    changeColor() {
      this.titleClass = 'red_title'
    },
  },
}
</script>

<template>
  <div>
    <h1 :class="titleClass">this is dynamic title with color class</h1>
    <button v-on:click="changeColor">click to change color</button>
  </div>
</template>

<style>
.green_title {
  color: green;
}
.red_title {
  color: red;
}
</style>
