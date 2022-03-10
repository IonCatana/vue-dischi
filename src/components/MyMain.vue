<template>
  <div id="mymain">
    <div class="container">
      <div class="card">
        <div class="img-titolo">
          <img src="../assets/spotify-logo.png" alt="" />
        </div>
        <div class="card-body">
          <h5 class="card-title">New Jarsey</h5>
          <p class="card-text">Bon Jovi</p>
          <p class="card-text">1988</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#mymain {
  width: 100vw;
  height: calc(100vh - 70px);
  background-color: #1e2d3b;
  display: flex;
}
.container {
  width: 60%;
  margin: 80px auto;
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
}
.card {
  width: 200px;
  height: 360px;
  background-color: #2e3a46;
}
.img-titolo {
  margin: 0 auto;
  margin-top: 20px;
  margin-bottom: 20px;
  width: 160px;
  height: 160px;
  aspect-ratio: 1;
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
.card-body {
  text-align: center;
}
</style>