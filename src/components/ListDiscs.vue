<template>
  <div v-if="loading">
    <LoaderDisc />
  </div>
  <div v-else class="row row row-cols-1 row-cols-md-2 row-cols-lg-5 g-5">
    <SingleDisc v-for="(disc, index) in albums" :key="index" :DiscObj="disc" />
  </div>
</template>
<script>
import SingleDisc from "./SingleDisc.vue";
import axios from "axios";
import LoaderDisc from "./LoaderDisc";
export default {
  name: "ListDiscs",
  components: {
    SingleDisc,
    LoaderDisc,
  },
  data: function () {
    return {
      albums: [],
      loading: true,
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((resp) => {
        this.albums = resp.data.response;
        this.loading = false;
      });
  },
};
</script>
<style lang="scss" scoped>
@import "../style/variables.scss";
div {
  background-color: $brand-primary-color;
}
</style>
