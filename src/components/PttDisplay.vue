<template>
  <div class="ptt-display">
    <v-btn
      tile
      plain
      class="ptt-btn btn"
    >
      <span class="btn-label">PTT</span>
    </v-btn>
    <div class="display mx-auto">
      <v-card
        class="my-5 d-flex radio justify-space-between"
        tile
        color="black"
        dark
        height="80%"
      >
        <v-btn
          class="left-arrow arrow align-self-center"
          plain
          tile
        >
          <v-icon
            class="icon"
            style="transform: rotate(180deg)"
          >
            mdi-play
          </v-icon>
        </v-btn>
        <div class="radio-display">
          radio
        </div>
        <v-btn
          class="right-arrow arrow align-self-center"
          tile
          plain
        >
          <v-icon class="icon">
            mdi-play
          </v-icon>
        </v-btn>
      </v-card>
    </div>
    <v-btn
      tile
      plain
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
    background-color: $mgs-dark-btn-green !important;
    -webkit-box-shadow: 0px 0px 0px 8px #000000;
    box-shadow: 0px 0px 0px 8px #000000;
    z-index: 2;
    height: 24px !important;
    left: 50%;
    transform: translateX(-50%);
    width: 160px;
    .btn-label {
      font-size: 22px;
      color: $mgs-mid-green;
      letter-spacing: 5px;
    }
  }
  .btn:hover .btn-label {
    color: $mgs-light-green !important;
  }
  .display {
    position: relative;
    border-top: solid $mgs-dark-green 2px;
    border-bottom: solid $mgs-dark-green 2px;
    width: 100%;
    height: 207px;
    top: -4px;
    .radio {
      .arrow {
        background-color: $mgs-dark-btn-green !important;
        height: 30px;
        min-width: 60px;
        padding: 0;
        .icon {
          color: $mgs-mid-green;
          font-size: 32px;
        }
      }
      .arrow:hover .icon {
        color: $mgs-light-green;
      }
    }
  }
}
</style>
