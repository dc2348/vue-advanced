<template>
  <div id="app">
    <!-- Strongly Recommended -->
    <!-- <ToolBar></ToolBar> -->
    <!--  Essential -->
    <tool-bar></tool-bar>
    <router-view></router-view>
    <!-- <NewView></NewView> -->
  </div>
</template>

<script>
import ToolBar from "./components/ToolBar.vue";
export default {
  components: {
    ToolBar,
  }
}
</script>


<style>
body {
  padding: 0;
  margin: 0;
}
</style>
