<template>
  <div class="codec">
    <Character />
    <PttDisplay />
    <Character />
    <ChatBox />
  </div>
</template>

<script>
import Character from '@/components/Character'
import PttDisplay from '@/components/PttDisplay'
import ChatBox from '@/components/ChatBox'
export default {
  components: {
    Character,
    PttDisplay,
    ChatBox
  }
}
</script>

<style lang="scss" scoped>
.codec {
  display: flex;
  margin: 0 auto;
  justify-content: space-evenly;
  border: solid #102018 1px;
  width: 800px;
  height: 450px;
  flex-wrap: wrap;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>
