<template>
  <section class="d-flex justify-content-center">
    <div
      class="disc text-center py-3 px-1 d-flex flex-column align-items-center"
    >
      <div class="disc__img"><img :src="DiscObj.poster" alt="" /></div>
      <h2 class="character-name mt-3">{{ DiscObj.title }}</h2>
      <p>{{ DiscObj.author }}</p>
      <p>{{ DiscObj.year }}</p>
    </div>
  </section>
</template>
<script>
export default {
  name: "SingleCard",
  props: {
    DiscObj: Object,
    index: Number,
  },
};
</script>
<style lang="scss" scoped>
@import "../style/variables.scss";
.disc {
  background-color: $brand-secondary-color;
  height: 350px;
  width: 300px;
  &__img {
    width: 150px;
    height: 150px;
    img {
      width: 100%;
      height: 100%;
    }
  }
  h2 {
    color: white;
    font-size: 1.6rem;
    text-transform: uppercase;
  }
  p {
    margin-bottom: 0;
    color: $text-color;
  }
}
</style>
