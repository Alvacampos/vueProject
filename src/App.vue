<template>
  <div id="app" class="wrapper">
    <div class="flex">
      <div>
        <New/>
      </div>
      <div class="main">
        <ProfileNav/>
        <EquityNav />
        <Overview />
      </div>
    </div>
  </div>
</template>

<script>
import Equity from "./components/Equity/Equity.vue";
import Profile from "./components/Profile/Profile.vue";
import SideDashboardVue from "./components/SideDashboard/SideDashboard.vue";
import Proximamente from "./components/Proximamente/Proximamente.vue";
import Content from "./components/Proximamente/Content.vue";
import New from "./components/SideDashboard/SideItem/New.vue";
import Overview from "./containers/Overview.vue";

export default {
  data() {
    return {
      selectedComponent: "Overview"
    };
  },
  components: {
    ProfileNav: Profile,
    SideDashboard: SideDashboardVue,
    EquityNav: Equity,
    Proximamente: Proximamente,
    Content: Content,
    New: New,
    Overview: Overview
  }
};
</script>

<style>
.main {
  margin-left: 280px; /* Same as the width of the sidenav */
  padding: 0px 10px;
}
</style>
