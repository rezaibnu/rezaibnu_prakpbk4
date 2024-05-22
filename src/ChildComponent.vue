<template>
    <div>
      <h2>PEKANBARU</h2>
      <NestedChildComponent @nested-data="emitData"/>
      <slot name="additional"></slot>
    </div>
  </template>
  
  <script>
  import NestedChildComponent from './NestedChildComponent.vue';
  
  export default {
    components: {
      NestedChildComponent
    },
    methods: {
      emitData(data) {
        this.$emit('data-emitted', data);
      }
    }
  }
  </script>
  