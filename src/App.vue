<template>
  <div id="app">
    <SpotiHeader />
    <SpotiMain />
  </div>
</template>

<script>
import SpotiHeader from "./components/SpotiHeader.vue";
import SpotiMain from "./components/SpotiMain.vue";
export default {
  name: "App",
  components: {
    SpotiHeader,
    SpotiMain,
  },
};
</script>
<style lang="scss">
@import "./style/commonStyle.scss";
@import "./style/variables.scss";
</style>
