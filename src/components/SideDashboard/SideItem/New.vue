<template>
      <ul class="sidenav">
      <li class="section" v-for="(section, i) in sections" :key="i">
        {{section.name}} 
        <ul>        
        <li v-for="(subsection, i) in section.subname" :key="i">{{subsection}} </li>
      </ul>
      </li>
    </ul>
</template>

<script>
export default {
  data() {
    return {
      sections: [
        {
          name: "DASHBOARD",
          subname: []
        },
        {
          name: "PROFILES",
          subname: []
        },
        {
          name: "PRODUCT ANALYSIS",
          subname: ["Compare", "Charting", "Style Analysis", "Style Reach"]
        },
        {
          name: "REPORTING",
          subname: ["Desing Lab", "Power Link", "Report book", "Workflow"]
        },
        {
          name: "MY DATA",
          subname: ["User Entered", "Portfolios"]
        },
        {
          name: "INSIGHTS",
          subname: [
            "Advantage",
            "Asset Flows",
            "Holdings Analysis",
            "Scorecard",
            "Universe Trends"
          ]
        },
        {
          name: "MANDATES",
          subname: ["Mandate Search"]
        }
      ]
    };
  }
};
</script>

<style scoped>
.sidenav {
  height: 100%;
  width: 280px;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: #444444;
  overflow-x: hidden;
  padding-top: 20px;
}

.sidenav li {
  padding: 6px 8px 6px 16px;
  text-decoration: none;
  font-size: 20px;
  color: #c7c7c7;
  display: block;
  list-style: none;
}

.section {
  border-top: white solid 1px;
  border-bottom: white solid 1px;
}

.sidenav a:hover {
  color: #f1f1f1;
}
</style>