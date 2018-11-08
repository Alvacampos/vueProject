<template>
  <div class="row">
    <div class="col" v-for="(value,index) in values" :key="index">
      <p>{{ value }}</p>
    </div>      
  </div>   
</template>

<script>
  export default {
    props: ['values']
  }  
</script>

<style scoped>
  p{
    margin: auto;
    padding: auto;
    font-size: 12px;
    font-family: 'Arimo', sans-serif;
  }
</style>