<template>
  <div id="app">
    <SpotiHeader @searchChange="searchChange($event)" />
    <SpotiMain :SearchStr="this.search" />
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
  data: function () {
    return {
      search: "All",
    };
  },
  methods: {
    searchChange(event) {
      // console.log(typeof event);
      this.search = event;
    },
  },
};
</script>
<style lang="scss">
@import "./style/commonStyle.scss";
@import "./style/variables.scss";
</style>
