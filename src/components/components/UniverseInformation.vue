<template>
  <div class="col">
    <div class="col" v-for="(value,index) in values" :key="index">
      <p>{{ value }}</p>      
        <hr/>        
    </div>
  </div>   
</template>

<script>
export default {
  props: ["values"]
};
</script>

<style scoped>
p {
  margin: auto;
  padding: auto;
  font-size: 12px;
  font-family: "Arimo", sans-serif;
}
</style>