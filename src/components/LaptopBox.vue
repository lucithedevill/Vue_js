<template>
    <div>
      <div v-for="laptop in laptops" :key="laptop._id">
        <SingleLaptop :laptop="laptop" />
      </div>
    </div>
  </template>
  
  <script>
  import SingleLaptop from './SingleLaptop.vue';
  
  export default {
    name: 'LaptopBox',
    props: {
      laptops: Array
    },
    components: {
      SingleLaptop
    }
  };
  </script>
  
  <style scoped>
  div {
    text-align: center;
  }
  </style>