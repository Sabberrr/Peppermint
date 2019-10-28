<template>
  <div id="app">
    <MainLoader v-if="this.$store.getters.getFileTree" />
    <!-- directly go to first page of the application on boot -->
    <ProjectLoader v-else />
  </div>
</template> 

<script>
import MainLoader from "./containers/MainLoader/MainLoader.vue";
import ProjectLoader from "./containers/ProjectLoader/ProjectLoader.vue";

export default {
  name: "peppermint",
  components: {
    MainLoader, // Main Page of the Application
    ProjectLoader // Title page of the application
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html,
body {
  height: 100%;
  width: 100% !important;
  /* max-height: 100%; */
  overflow: hidden !important;
}

#app {
  /* overflow: hidden !important; */
  height: 100%;
  width: 100%;

  /* color schema one */
  background-color: #232323;
}

button {
  cursor: pointer;
}
</style>
