<template>
    <div>
      <h2 class="text-xl mb-2">Uncle Component</h2>
      <button @click="sendData" class="bg-orange-500 text-white px-4 py-2 rounded">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendData() {
        this.$emit('sendData', 'Message from Uncle');
      },
    },
  };
  </script>
  
  <style scoped>
  h2 {
    color: #708240;
  }
  button {
    background-color: #708240;
  }
  </style>
  