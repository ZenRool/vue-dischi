<template>
  <header class="header container-fluid">
    <div class="header__logo row align-items-center">
      <div class="offset-1 col-1 h-75">
        <img src="../assets/img/logo.png" alt="logo" />
      </div>
      <div class="offset-7 col-2">
        <SearchGenre />
      </div>
    </div>
  </header>
</template>
<script>
import SearchGenre from "./SearchGenre.vue";
export default {
  name: "SpotiHeader",
  components: {
    SearchGenre,
  },
};
</script>
<style lang="scss" scoped>
@import "../style/variables.scss";
.header {
  height: 90px;
  background-color: $brand-secondary-color;
  &__logo {
    height: 100%;
    img {
      height: 100%;
      width: auto;
    }
  }
}
</style>
