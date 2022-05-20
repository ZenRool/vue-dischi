<template>
  <select name="genre" id="genre">
    <option value="all">All</option>
    <option value="Pop">Pop</option>
    <option value="Rock">Rock</option>
    <option value="Metal">Metal</option>
    <option value="Jazz">Jazz</option>
  </select>
</template>
<script>
export default {
  name: "SearchGenre",
};
</script>
<style lang="scss" scoped>
@import "../style/variables.scss";
select {
  width: 80%;
  font-size: 1.6rem;
  background-color: $brand-primary-color;
  color: white;
  border-color: lime;
  border-radius: 5px;
}
</style>
