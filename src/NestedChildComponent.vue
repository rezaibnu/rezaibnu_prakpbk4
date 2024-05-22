<template>
    <div>
      <h3>RIAU</h3>
      <button @click="sendData">Kirim Data ke Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendData() {
        const data = 'Data dari NestedChildComponent';
        this.$emit('nested-data', data);
      }
    }
  }
  </script>
  