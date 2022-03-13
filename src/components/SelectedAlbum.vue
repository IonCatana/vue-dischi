<template>
  <form>
    <select
      v-model="selected"
      class="form-selected"
      aria-label=""
      @change.prevent="$emit('selectedAlbums', selected)"
    >
      <option value="">Choose genre...</option>
      <option value="All">All albums</option>
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Jazz">Jazz</option>
      <option value="Metal">Metal</option>
    </select>
  </form>
</template>

<script>
export default {
  data() {
    return {
      selected: "",
    };
  },
  methods: {
    selectedAlbums(optionSelected) {
      console.log(optionSelected)
      console.log(this.selected)
    },
  },
};
</script>

<style lang="scss" scoped>
form{
  padding-top: 40px;
  text-align: center;
}
select{
  width: 200px;
  padding: 5px 10px;
  border-radius: 10px;
}
</style>