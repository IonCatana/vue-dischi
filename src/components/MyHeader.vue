<template>
  <div id="my-header">
    <div class="logo">
      <img src="../assets/spotify-logo.png" alt="" />
    </div>
    <div class="titolo">
      <h1>Vue Dischi</h1>
    </div>
    
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#my-header {
  width: 100vw;
  background-color: #2e3a46;
  min-height: 70px;
  display: flex;
  align-items: center;
}
.logo {  
  display: flex;    
  width: 50px;
  margin-left: 20px;
}
.titolo{
  height: 70px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  width: calc(100% - 70px);
  h1{
    font-size: 40px;
    font-weight: 800;
  }
}
</style>