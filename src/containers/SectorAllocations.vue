<template>
  <div>
    <div>
      <h1 style="margin-top: 50px">Sector Allocations</h1>        
    </div>
    <div class="" style="margin: 5px">
      <div class="container-full">
        <app-titles :titles="titles" style="margin: 5px"></app-titles>
        <hr/>
        <div class="col" v-for="(element,key) in profileData" :key="key">
          <app-infomation :values="element"></app-infomation>
          <hr/>
        </div>
      </div>      
    </div>    
  </div>  
</template>

<script>
import Titles from "../components/components/Titles.vue";
import Information from "../components/components/Information.vue";
export default {
  data() {
    return {
      titles: ["Sector", "Allocation(%)"],
      profileData: {          
        sectorFinancialServices: ["Financial Services", 29.61 + "%"],
        sectorProducerDurables: ["Producer Durables", 28.61 + "%"],
        sectorConsumerDiscretionary: ["Consumer Discretionary", 29.61 + "%"],
        sectorTechnology: ["Technology", 28.61 + "%"],
        sectorMaterials: ["Materials & Processing", 29.61 + "%"],
        sectorHealthCare: ["Health Care", 28.61 + "%"],
        sectorEnergy: ["Energy", 29.61 + "%"],
        sectorUtilities: ["Utilities", 28.61 + "%"],
        sectorConsumer: ["Consumer Staples", 28.61 + "%"]
      }
    }    
  },
  components: {
    "app-titles": Titles,
    "app-infomation": Information
  }
};
</script>

<style scoped>
h1 {
  color: #072767;
  background-color: #dcdcdc;
  padding: 5px 25px;
  font-size: 15px;
  font-weight: bold;
  font-family: "Arimo", sans-serif;
}
</style>