<template>
  <div>
    <h1>Growth of $100: 5 Year</h1>
    <div class="row">
      <img src="https://www.amcharts.com/wp-content/uploads/2013/12/demo_7395_light.jpg" alt="Img">
    </div>
    <div class="row" style="margin: 5px">
      <div class="container-full">
        <app-titles :titles="titles"></app-titles>
        <hr/>        
        <div class="col" v-for="(element,key) in profileData" :key="key">
          <app-information :values="element"></app-information>
          <hr/>  
        </div>  
      </div>
    </div>    
  </div>  
</template>

<script>
import Information from "../components/components/Information.vue";
import Titles from "../components/components/Titles.vue";
export default {
  data() {
    return {
      titles: [
        "Product",
        "5 Year Growth of $100",
        "5 Year Growth of $100 High",
        "5 Year Growth of $100 Low",
        "5 Year Cumulative Performance",
        "5 Year Annual Performance",
        "5 Year Max Drawdown"
      ],
      profileData: {
        usSmallValue: [
          "US Small-Mid Cap Value Equity",
          29.61 + "%",
          13.62,
          13.62,
          13.62,
          13.62,
          13.62
        ],
        russellValue: [
          "Russell 2500 Value",
          28.61 + "%",
          1.59,
          1.59,
          1.59,
          1.59,
          1.59
        ]
      }            
    };
  },
  components: {
    "app-information": Information,
    "app-titles": Titles
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

  img {
    display: block;
    margin: 20px auto;
    height: 400px;
    width: 75%;
  }
  
  .titles {
    margin: 10px;
    font-family: "Arimo", sans-serif;
  }

  .container-full {
    margin: 0 auto;
    width: 100%;
  }
</style>