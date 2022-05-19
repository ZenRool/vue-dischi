<template>
  <div id="app">
    <SpotiHeader />
  </div>
</template>

<script>
import SpotiHeader from "./components/SpotiHeader.vue";
export default {
  name: "App",
  components: {
    SpotiHeader,
  },
};
</script>
<style lang="scss">
@import "./style/commonStyle.scss";
@import "./style/variables.scss";
</style>
