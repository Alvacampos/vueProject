<template>
  <div class="container-full">
    <div class="container-full">
      <div class="row">
        <div class="col-12">
          <app-growth></app-growth>
          <app-sector></app-sector>
          <app-universe></app-universe>
          <hr>
          <app-footer></app-footer>    
        </div>  
      </div>        
    </div>       
  </div>
</template>

<script>
import Footer from "../components/components/Footer.vue";
import Universe from "./Universe.vue";
import Growth from "./Growth.vue";
import SectorAllocations from "./SectorAllocations.vue";

export default {
  components: {
    "app-growth": Growth,
    "app-sector": SectorAllocations,
    "app-footer": Footer,
    "app-universe": Universe
  }
};
</script>

<style scoped>
.container-full {
  margin: 0 auto;
  width: 100%;
}
</style>