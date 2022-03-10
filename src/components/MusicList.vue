<template>
  
    
      <div class="card">
        <div class="img-titolo">
          <img :src="MusicList.poster" alt="" />
        </div>
        
          <h5 class="card-title">{{ MusicList.title}}</h5>
          <p class="card-text">{{ MusicList.author }}</p>
          <p class="card-text">{{ MusicList.year }}</p>
        
      </div>
    
 
</template>

<script>
export default {
  props: {
    MusicList: {
      type: Object,
      require: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.card {
  padding: 20px;
  text-align: center;
  width: calc((100% / 5 ) - 30px);
  min-height: 360px;
  background-color: #2e3a46;
}
.img-titolo {   
  display: block;
  aspect-ratio: 1/1 ;  
}
h5{
  margin-top: 20px;
}
.card-title {
  color: white;
  text-transform: uppercase;
  font-size: 23px;
  padding-bottom: 20px;
}
.card-text {
  color: grey;
  font-size: 19px;
}

</style>