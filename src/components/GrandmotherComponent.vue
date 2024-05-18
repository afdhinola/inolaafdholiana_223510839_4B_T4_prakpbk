<template>
    <div>
      <h2 class="text-xl mb-2">Grandmother Component</h2>
      <button @click="sendData" class="bg-purple-500 text-white px-4 py-2 rounded">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendData() {
        this.$emit('sendData', 'Message from Grandmother');
      },
    },
  };
  </script>
  
  <style scoped>
  h2 {
    color: #F49069;
  }
  button {
    background-color:#F49069 ;
  }
  </style>
  