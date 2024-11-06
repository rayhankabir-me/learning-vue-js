<script>
export default {
  data() {
    return {
      text: '',
    }
  },
  methods: {
    onInput(e) {
      this.text = e.target.value
    },
  },
}
</script>
<template>
  <div>
    <input
      :value="text"
      @input="onInput"
      type="text"
      placeholder="type your name"
    />
    <p>{{ text }}</p>
  </div>
</template>
