<template>
  <div id="my-main">
    <div>
      <SelectedAlbum @selectedAlbums="select" />
    </div>
    <div class="music-list">
      <MusicList v-for="(el, i) in MusicLists" :key="i" :MusicList="el" />
    </div>
  </div>
</template>

<script>
import MusicList from "./MusicList.vue";
import SelectedAlbum from "../components/SelectedAlbum.vue";
import axios from "axios";
export default {
  components: {
    SelectedAlbum,
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
    select(elementoSelezionato) {
      console.log(elementoSelezionato);
      this.optionSelected = elementoSelezionato;
    },
  },
  computed: {
    getFilteredAlbums() {
      if (this.optionSelected === "All") {
        return this.MusicList;
      }
      const filteredAlbums = this.MusicList.filter((poster) => {
        return poster.genre.inludes(this.optionSelected);
      });
      return filteredAlbums;
    },
  },
  created() {
    this.fetchMusicList();
  },
};
</script>

<style lang="scss" scoped>
.music-list {
  width: 80%;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
  padding: 40px;
  height: 100vh;
}
</style>