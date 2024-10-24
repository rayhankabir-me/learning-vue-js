<script>
export default {
  data() {
    return {
      count: 0,
    }
  },
  methods: {
    counterPlus() {
      this.count++
    },
  },
}
</script>

<template>
  {{ count }}
  <button @click="counterPlus">click here</button>
</template>
