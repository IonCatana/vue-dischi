<template>
  <div id="my-header">
    <div class="logo">
      <img src="../assets/spotify-logo.png" alt="" />
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
  align-items: center;
  width: 50px;
  margin-left: 20px;
}
</style>