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
      @click="freqControll('dec')"
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
      class="radio-display-frame"
    >
      <v-sheet
        width="205px"
        height="149px"
        class="radio-display"
      >
        <div class="radio-freq">
          <span
            class="freq freq-shadow"
          ><span class="freq-small">00</span>0.00</span>
          <span
            class="freq"
          ><span class="freq-small">{{ radioFreqSmall }}</span>{{ radioFreqBig }}</span>
        </div>
        <div class="radio-graph-bars pa-1">
          <v-sheet
            v-for="(bar, index) in radioGraphBars"
            :key="index"
            :class="bar.active ? 'bar-active' : 'bar-inactive'"
            class="bar"
            height="13.4px"
          />
        </div>
      </v-sheet>
    </v-sheet>
    <v-btn
      class="right-arrow arrow pa-0 align-self-center"
      min-width="60px"
      height="30px"
      tile
      plain
      @click="freqControll('inc')"
    >
      <!-- @click="freqControll('inc')" -->
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
      radioFreq: 14085,
      radioGraphBars: []
    }
  },
  computed: {
    radioFreqSmall: function() {
      return String(this.radioFreq).slice(0, 2)
    },
    radioFreqBig: function() {
      let withDot = String(this.radioFreq).slice(2)
      withDot = withDot.split('')
      withDot.splice(1, 0, '.')
      withDot = withDot.join('')
      return withDot
    }
  },
  created() {
    for (let index = 0; index < 9; index++) {
      // this.radioGraphBars.push({ active: true })
      if (index > 1) this.radioGraphBars.push({ active: true })
      else this.radioGraphBars.push({ active: false })
    }
  },
  methods: {
    freqControll(incOrDec) {
      if (incOrDec === 'inc') this.radioFreq++
      if (incOrDec === 'dec') this.radioFreq--
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
  .radio-display-frame {
    background-color: $mgs-dark-green;
    .radio-display {
      -webkit-box-shadow: 0px 10px 0px -5px #000000, 0px -10px 0px -5px #000000,
        -10px 0px 0px 3px #000000, 16px 0px 0px 3px #000000;
      box-shadow: 0px 10px 0px -5px #000000, 0px -10px 0px -5px #000000,
        -10px 0px 0px 3px #000000, 10px 0px 0px 3px #000000;
      position: relative;
      top: 7px;
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
          font-family: 'digital-7';
          bottom: -21px;
          left: 32px;
          font-size: 60px;
          letter-spacing: 2px;
          position: absolute;
          .freq-small {
            font-size: 50px;
          }
        }
        .freq-shadow {
          color: $mgs-mid-green;
          left: 16.5px;
        }
      }
      .radio-graph-bars {
        .bar {
          margin: 2px 0;
        }
        .bar-active {
          background-color: $mgs-light-green;
        }
        .bar-inactive {
          background-color: $mgs-mid-green;
        }
      }
    }
  }
}
</style>
