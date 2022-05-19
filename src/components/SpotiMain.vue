<template>
  <main class="main container-fluid">
    <div class="container d-flex align-items-center justify-content-center">
      <ListDiscs />
    </div>
  </main>
</template>
<script>
import ListDiscs from "./ListDiscs.vue";
export default {
  name: "SpotiMain",
  components: {
    ListDiscs,
  },
};
</script>
<style lang="scss" scoped>
@import "../style/variables.scss";
.main {
  min-height: calc(100vh - 90px);
  padding-top: 90px;
  background-color: $brand-primary-color;
}
</style>
