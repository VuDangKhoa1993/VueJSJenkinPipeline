<template>
  <div>
    <the-header></the-header>
    <!-- <badge-list></badge-list>
    <user-info
      :full-name="activeUser.name"
      :info-text="activeUser.description"
      :role="activeUser.role"
    ></user-info> -->
    <button @click="onSelectedComponent('active-goal')">Active Goal</button>
    <button @click="onSelectedComponent('manage-goal')">Manage Goal</button>
    <keep-alive>
    <component :is="selectedComponent"></component>
    </keep-alive>
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
// import BadgeList from "./components/BadgeList.vue";
// import UserInfo from "./components/UserInfo.vue";
import ActiveGoal from './components/ActiveGoal.vue';
import ManageGoal from './components/ManageGoal.vue'
export default {
  components: {
    TheHeader,
    // BadgeList,
    // UserInfo,
    ActiveGoal,
    ManageGoal
  },
  data() {
    return {
      selectedComponent: 'active-goal',
      activeUser: {
        name: "Maximilian Schwarzmüller",
        description: "Site owner and admin",
        role: "admin",
      },
    };
  },
  methods: {
    onSelectedComponent(cpm) {
      this.selectedComponent = cpm;
    }
  }
};
</script>

<style>
html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>
