<template>
  <div class="loader-disc">
    <span></span>
    <span></span>
    <span></span>
    <div></div>
  </div>
</template>
<script>
export default {
  name: "LoaderDisc",
};
</script>
<style lang="scss" scoped>
@import "../style/variables.scss";
.loader-disc {
  width: 4rem;
  position: relative;
  display: flex;
  justify-content: space-between;
  margin: 0;
  span {
    content: "a";
    width: 1rem;
    height: 3rem;
    background-color: lime;
    border-radius: 8px;
    transform-origin: bottom;
    animation: bounce 2.2s ease infinite alternate;
    &:nth-of-type(2) {
      animation-delay: -2.2s;
    }
    &:nth-of-type(3) {
      animation-delay: -3.7s;
    }
  }
}
@keyframes bounce {
  10% {
    transform: scaleY(0.3);
  }
  30% {
    transform: scaleY(1); /* scale up to 100% */
  }
  60% {
    transform: scaleY(0.5); /* scale down to 50% */
  }
  80% {
    transform: scaleY(0.75); /* scale up to 75% */
  }
  100% {
    transform: scaleY(0.6); /* scale down to 60% */
  }
}
</style>
