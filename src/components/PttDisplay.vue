<template>
  <div class="ptt-display">
    <v-btn
      tile
      color="#101818"
      class="btn-ptt"
    >
      <span class="btn-label ptt">PTT</span>
    </v-btn>
    <div class="display mx-auto">
      content
    </div>
    <div class="btn-wrapper">
      <v-btn
        tile
        color="#101818"
        class="btn-ptt"
      >
        <span class="btn-label ptt">MEMORY</span>
      </v-btn>
    </div>
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
  .display {
    border-top: solid #102018 2px;
    border-bottom: solid #102018 2px;
    width: 90%;
    height: 177px;
  }
}
</style>
