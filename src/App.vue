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
.app {
  background-color: #000000 !important;
  color: #ffffff !important;
}
</style>
