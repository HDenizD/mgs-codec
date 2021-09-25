<template>
  <v-card
    class="my-5 d-flex radio justify-space-between"
    tile
    color="black"
    height="80%"
  >
    <v-btn
      class="left-arrow arrow pa-0 align-self-center"
      min-width="60px"
      height="30px"
      plain
      tile
    >
      <v-icon
        class="icon"
        style="transform: rotate(180deg)"
        size="32px"
      >
        mdi-play
      </v-icon>
    </v-btn>
    <v-sheet
      width="90%"
      height="100%"
      class="radio-display mx-3"
    >
      <div class="radio-freq">
        <span class="freq"><span class="freq-small">14</span>0.85</span>
      </div>
      <div class="radio-graph-bars pa-1">
        <v-sheet
          v-for="(bar, index) in radioGraphBars"
          :key="index"
          class="bar"
          height="17.2px"
        />
      </div>
    </v-sheet>
    <v-btn
      class="right-arrow arrow pa-0 align-self-center"
      min-width="60px"
      height="30px"
      tile
      plain
    >
      <v-icon
        class="icon"
        size="32px"
      >
        mdi-play
      </v-icon>
    </v-btn>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      radioGraphBars: []
    }
  },
  created() {
    for (let index = 0; index < 9; index++) {
      this.radioGraphBars.push({ active: false })
    }
  }
}
</script>

<style lang="scss" scoped>
.radio {
  width: 100%;
  .arrow {
    background-color: $mgs-dark-btn-green;
    .icon {
      color: $mgs-mid-green;
    }
  }
  .arrow:hover .icon {
    color: $mgs-light-green;
  }
  .radio-display {
    position: relative;
    width: 100%;
    background-color: $mgs-dark-green;
    color: $mgs-light-green;
    margin: 0 auto;
    .radio-freq {
      position: absolute;
      z-index: 10;
      background-color: $mgs-dark-green;
      bottom: 3px;
      right: 0px;
      width: 85%;
      height: 85%;
      border-top-left-radius: 140px;
      .freq {
        bottom: -10px;
        left: 32px;
        font-size: 50px;
        position: absolute;
        .freq-small {
          font-size: 35px;
        }
      }
    }
    .radio-graph-bars {
      .bar {
        background-color: $mgs-light-green;
      }
    }
  }
}
</style>
