<template>
  <div class="codec">
    <Character />
    <Character />
  </div>
</template>

<script>
import Character from '@/components/Character'
export default {
  components: {
    Character
  }
}
</script>

<style lang="scss" scoped>
.codec {
  background-color: #000000;
  height: 100%;
}
</style>
