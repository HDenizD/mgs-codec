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
      >
        mdi-play
      </v-icon>
    </v-btn>
    <v-sheet
      width="90%"
      height="100%"
      class="radio-display mx-3"
    >
      <div class="radio-bars pa-1">
        radio graph
      </div>
    </v-sheet>
    <v-btn
      class="right-arrow arrow pa-0 align-self-center"
      min-width="60px"
      height="30px"
      tile
      plain
    >
      <v-icon class="icon">
        mdi-play
      </v-icon>
    </v-btn>
  </v-card>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.radio {
  width: 100%;
  .arrow {
    background-color: $mgs-dark-btn-green !important;
    .icon {
      color: $mgs-mid-green;
      font-size: 32px;
    }
  }
  .arrow:hover .icon {
    color: $mgs-light-green;
  }
  .radio-display {
    width: 100%;
    background-color: $mgs-dark-green;
    color: $mgs-light-green;
    margin: 0 auto;
  }
}
</style>
