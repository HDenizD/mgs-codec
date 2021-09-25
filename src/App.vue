<template>
  <v-app class="app">
    <Codec />
  </v-app>
</template>

<script>
import Codec from '@/components/Codec'
export default {
  name: 'App',
  components: {
    Codec
  },
  data: () => ({
    //
  })
}
</script>
<style lang="scss">
html {
  overflow-y: auto;
}
.app {
  background-color: #000000 !important;
  color: #ffffff !important;
}
@font-face {
  font-family: "digital-7";
  src: local("digital-7"),
   url(./fonts/digital-7.ttf) format("truetype");
}
</style>
