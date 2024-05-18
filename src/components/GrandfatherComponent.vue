<template>
  <div>
    <h2 class="text-xl mb-2">Grandfather Component</h2>
    <button @click="sendData" class="bg-red-500 text-white px-4 py-2 rounded">Send Data to Parent</button>
  </div>
</template>

<script>
export default {
  methods: {
    sendData() {
      this.$emit('sendData', 'Message from Grandfather');
    },
  },
};
</script>

<style scoped>
h2 {
  color: #FEDC7B;
}
button {
  background-color: #f8ce5c;
}
</style>
