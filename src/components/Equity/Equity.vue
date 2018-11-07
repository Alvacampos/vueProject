<template>
    <div>
        <h2>All global Equity</h2>
        <ul class="nav">
            <li class="nav-item" v-for="link in links" >
                <a class="nav-link" href="#" @click="selectedComponent = '{{link}}'" >{{link}}</a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        "Overview",
        "Performance",
        "Asset Flows",
        "Universe Comparison",
        "Constituents",
        "Constituent Holdings",
        "Sector Allocation",
        "Ownership Activity"
      ]
    };
  }
};
</script>

<style>
</style>
