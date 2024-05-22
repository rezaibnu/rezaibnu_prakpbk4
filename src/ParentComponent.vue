<template>
    <div>
      <h1>UNIVERSITAS ISLAM RIAU</h1>
      <ChildComponent @data-emitted="handleData">
        <template v-slot:additional>
          <p>Ini adalah konten slot yang disisipkan ke dalam ChildComponent</p>
        </template>
      </ChildComponent>
      <p>Data dari komponen nested: {{ nestedData }}</p>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    components: {
      ChildComponent
    },
    data() {
      return {
        nestedData: ''
      };
    },
    methods: {
      handleData(data) {
        this.nestedData = data;
      }
    }
  }
  </script>
  