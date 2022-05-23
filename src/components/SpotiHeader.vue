<template>
  <header class="header container-fluid">
    <div class="header__logo row align-items-center">
      <div class="offset-1 col-1 h-75">
        <img src="../assets/img/logo.png" alt="logo" />
      </div>
      <div class="offset-lg-7 col-lg-2 offset-md-6 col-md-3 offset-5 col-4">
        <SearchGenre @searchChange="searchChange($event)" />
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
  methods: {
    searchChange(event) {
      this.$emit("searchChange", event);
      // console.log(typeof event);
    },
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
