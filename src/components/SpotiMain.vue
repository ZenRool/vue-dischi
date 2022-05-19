<template>
  <main
    class="main container-fluid d-flex align-items-center justify-content-center"
  >
    <div class="container"></div>
  </main>
</template>
<script>
export default {
  name: "SpotiMain",
};
</script>
<style lang="scss" scoped>
@import "../style/variables.scss";
.main {
  height: calc(100vh - 90px);
  background-color: $brand-primary-color;
  .container {
    background-color: red;
    height: 100px;
  }
}
</style>
