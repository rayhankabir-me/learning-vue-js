<script>
export default {
  data() {
    return {
      inputData: '',
    }
  },
}
</script>

<template>
  <div>
    <input v-model="inputData" placeholder="Type here" />
    {{ inputData }}
    {{ console.log('code is running..!') }}
  </div>
</template>
