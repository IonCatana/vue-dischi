<template>
  <div id="my-main">
    <MusicList v-for="(el, i) in MusicLists" :key="i" :MusicList="el" />
  </div>
</template>

<script>
import MusicList from "./MusicList.vue";
import axios from "axios";
export default {
  components: {
    MusicList,
  },
  data() {
    return {
      MusicLists: [],
    };
  },

  methods: {
    fetchMusicList: function () {
      axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((res) => {
          console.log(res.data);
          this.MusicLists = res.data.response;
        })
        .catch((err) => {
          console.warn(err.response);
        });
    },
  },
  created() {
    this.fetchMusicList();
  },
};
</script>

<style lang="scss" scoped>
#my-main {
  width: 80%;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
  padding: 40px;
}
</style>