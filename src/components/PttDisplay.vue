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
      <v-card
        class="my-5"
        tile
        color="black"
        dark
        height="80%"
      >
        display
        <v-sheet
          color="green"
          height="20px"
          width="20px"
        />
      </v-card>
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
      color: $mgs-light-green;
      letter-spacing: 5px;
    }
  }
  .display {
    position: relative;
    border-top: solid $mgs-dark-green 2px;
    border-bottom: solid $mgs-dark-green 2px;
    width: 95%;
    height: 207px;
    top: -4px;
  }
}
</style>
