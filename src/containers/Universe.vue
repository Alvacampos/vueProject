<template>
  <div>
    <h1>Peer Universe Information</h1>        
    <div class="row" style="margin: 5px">
      <div class="container-full">               
        <div class="row">
          <app-information :values="universeInformation">
          </app-information>  
        </div>        
      </div>
    </div>    
  </div>  
</template>

<script>
import UniverseInformation from "../components/components/UniverseInformation.vue";
export default {
  data() {
    return {
      universeInformation: [
        "Unique Equity Securities",
        "Number of Securities in avg Portfolio",
        "Cash",
        "Larges Position",
        "Most Widely Held Position"
      ]
    };
  },
  components: {
    "app-information": UniverseInformation
  }
};
</script>

<style scoped>
h1 {
  color: #072767;
  background-color: #dcdcdc;
  padding: 5px 20px;
  font-size: 15px;
  font-weight: bold;
  font-family: "Arimo", sans-serif;
}
.container-full {
  margin: 0 auto;
  width: 100%;
}
</style>