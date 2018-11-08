<template>
  <div class="row titles">
    <div class="col" v-for="(title,index) in titles" :key="index">
      <h5>{{ title }}</h5>
    </div>                    
  </div>
</template>

<script>
  export default {
    props: ['titles']
  }  
</script>

<style scoped> 
  h5 {
    font-size: 13px;
    font-family: 'Arimo', sans-serif;
  }

</style>