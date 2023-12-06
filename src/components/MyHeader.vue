<template>
    <div>
      <h1>{{ appName }}</h1>
      <h2>{{ authorName }}</h2>
    </div>
  </template>
  
  <script>
  export default {
    name: 'MyHeader',
    props: {
      appName: String,
      authorName: String
    }
  };
  </script>
  
  <style scoped>
  div {
    text-align: center;
  }
  </style>