<template>
    <div>
      <h2 class="text-xl mb-2">Aunt Component</h2>
      <button @click="sendData" class="bg-teal-500 text-white px-4 py-2 rounded">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendData() {
        this.$emit('sendData', 'Message from Aunt');
      },
    },
  };
  </script>
  
  <style scoped>
  h2 {
    color: #ABBA72;
  }
  button {
    background-color: #ABBA72;
  }
  </style>
  