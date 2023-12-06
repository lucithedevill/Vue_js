<template>
    <div :class="laptop['Is available'] ? 'yes' : 'no'">
      <h2>{{ laptop.Company }}</h2>
      <h2>{{ laptop.OperatingSystem }}</h2>
      <h2>{{ laptop.RAMSize }}</h2>
      <h2>{{ laptop.Price }}</h2>
      <h3>Manufacturer Details:</h3>
    <p>Series: {{ laptop.Manufacturer_details.Series }}</p>
    <p>Year: {{ laptop.Manufacturer_details.Year }}</p>
    </div>
  </template>
  
  
  <script>
  export default {
    name: 'SingleLaptop',
    props: {
      laptop: Object
    }
  };
  </script>
  
  <style scoped>
  
  
  div:hover {
  transform: scale(1.02); 
}
.yes {
    background-color: rgb(51, 0, 128);
  }
  
  h2 {
    font-size: 2em;
    color: white;
  }
  
  div {
    background-color: #752d13;
    color: rgb(237, 229, 229);
    padding: 1em;
    text-align: center;
    margin: 1em;
  }
  
  .no {
    background-color: rgb(151, 114, 45) !important;
  }
 
  </style>