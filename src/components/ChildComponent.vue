<template>
  <div>
    <h2 class="text-xl mb-2">Child Component</h2>
    <button @click="sendData" class="bg-gray-700 text-white px-4 py-2 rounded">Send Data to Parent</button>
  </div>
</template>

<script>
export default {
  methods: {
    sendData() {
      this.$emit('sendData', 'Message from Child');
    },
  },
};
</script>

<style scoped>
h2 {
  color: #D76149;
}
button {
  background-color: #D76149;
}
</style>
