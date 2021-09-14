<template>
  <div class="ptt-display">
    <v-btn
      tile
      color="#101818"
      class="ptt-btn btn"
    >
      <span class="btn-label">PTT</span>
    </v-btn>
    <div class="display mx-auto">
      content
    </div>
    <v-btn
      tile
      color="#101818"
      class="memory-btn btn"
    >
      <span class="btn-label">MEMORY</span>
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
  .ptt-btn {
    position: relative;
    top: -2px;
  }
  .memory-btn {
    position: relative;
    bottom: 6px;
  }
  .btn {
    -webkit-box-shadow: 0px 0px 0px 8px #000000;
    box-shadow: 0px 0px 0px 8px #000000;
    z-index: 2;
    height: 24px !important;
    left: 50%;
    transform: translateX(-50%);
    width: 160px;
    .btn-label {
      font-size: 22px;
      color: #98f8d0;
      letter-spacing: 5px;
    }
  }
  .display {
    position: relative;
    border-top: solid #102018 2px;
    border-bottom: solid #102018 2px;
    width: 95%;
    height: 207px;
    top: -4px;
  }
}
</style>
