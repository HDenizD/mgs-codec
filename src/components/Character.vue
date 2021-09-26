<template>
  <div class="character">
    <v-img
      :src="charImg"
      height="100%"
    />
  </div>
</template>

<script>
export default {
  props: {
    charImg: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.character {
  -webkit-box-shadow: 0px 0px 12px 0px #237c57;
  box-shadow: 0px 0px 12px 0px #237c57;
  height: 250px;
  width: 150px;
  z-index: 10;
  // background-color: #307850;
}
</style>
