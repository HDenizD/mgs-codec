<template>
  <div class="codec">
    <Character :char-img="campbell" />
    <PttDisplay />
    <Character :char-img="snake" />
    <ChatBox />
  </div>
</template>

<script>
import Character from '@/components/Character'
import PttDisplay from '@/components/PttDisplay'
import ChatBox from '@/components/ChatBox'

import snake from '@/assets/snake.png'
import campbell from '@/assets/campbell.png'

export default {
  components: {
    Character,
    PttDisplay,
    ChatBox
  },
  data() {
    return {
      campbell: campbell,
      snake: snake
    }
  }
}
</script>

<style lang="scss" scoped>
.codec {
  display: flex;
  margin: 0 auto;
  justify-content: space-evenly;
  border: solid #102018 2px;
  width: 700px;
  height: 253px;
  flex-wrap: wrap;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>
