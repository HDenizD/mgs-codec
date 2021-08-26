<template>
  <div class="ptt-display">
    <v-btn
      tile
      color="#101818"
      class="btn-ptt"
    >
      <span class="btn-label ptt">PTT</span>
    </v-btn>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.ptt-display {
  background-color: #000000;
  width: 350px;
  height: 238px;
  .btn-ptt {
    left: 50%;
    transform: translateX(-50%);
    width: 200px;
    .ptt {
      font-size: 35px;
      color: #98f8d0;
      letter-spacing: 5px;
    }
  }
}
</style>
