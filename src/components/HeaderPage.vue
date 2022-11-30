<template>
  <div class="container-fluid p-0 ctnmain">
    <div class="divheader py-2">
      <img src="../assets/spotify-logo-png-7053.png" alt="spotify-logo" class="logo">
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderPage',
};
</script>

<style lang="scss" scoped>
$main_color_1: #2E3A46;
$main_color_2: #1E2D3B;
.ctnmain{
  height: 100%;
}
.divheader{
  background-color: $main_color_1;
  height: 100%;
}
.logo{
  width: 35px;
  margin-left: 1rem;
}
</style>
