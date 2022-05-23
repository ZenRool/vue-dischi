<template>
  <select
    name="genre"
    id="genre"
    v-model="selected"
    @change="$emit('searchChange', selected)"
  >
    <option value="All">All</option>
    <option value="Pop">Pop</option>
    <option value="Rock">Rock</option>
    <option value="Metal">Metal</option>
    <option value="Jazz">Jazz</option>
  </select>
</template>
<script>
export default {
  name: "SearchGenre",
  data: function () {
    return {
      selected: "all",
    };
  },
};
</script>
<style lang="scss" scoped>
@import "../style/variables.scss";
select {
  min-width: 100%;
  font-size: 1.6rem;
  background-color: $brand-primary-color;
  color: white;
  border-color: lime;
  border-radius: 5px;
}
</style>
