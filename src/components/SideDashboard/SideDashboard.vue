<template>
<div class="sidenav">
  <li v-for="(item, i) in items" :key="i">{{item}}</li>
</div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        "DASHBOARD",
        "SCREEN",
        "PRODUCT ANALYSIS",
        "REPORTING",
        "MY DATA",
        "INSIGHTS",
        "MANDATES"
      ]
    };
  }
};
</script>

<style scoped>
.sidenav {
  height: 100%;
  width: 180px;
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

.sidenav a:hover {
  color: #f1f1f1;
}
</style>

