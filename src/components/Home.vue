<template>
  <div class="home">
    <div class="home-text fadeInUp animated">
      Join the lucky game for a chance to receive
      <br/><span class="orange fadeIn animated delay-1s"><span class="f40">100</span> TOMO</span>
    </div>
    <div v-if="!winner && (finishBlock > currentBlock)" >
      <button class="btn fadeInUp animated delay-1s" @click="$emit('join')">Join now</button>
      <br/>
      <a v-if="isJoined" class="home-go-to-game fadeInUp animated delay-2s" @click="$emit('game')">view result</a>
    </div>
    <div v-else>
      <button class="btn fadeInUp animated delay-1s" @click="$emit('game')">View result</button>
    </div>
  </div>
</template>
<script>
export default {
  props: ['winner', 'finishBlock', 'currentBlock', 'isJoined']
}
</script>

<style>
.home {
  margin-top: 70px;
}

.home-text {
  font-size: 25px;
  margin-bottom: 50px;
}

.home-go-to-game {
  margin-top: 10px;
  display: inline-block;
  color: #F36E2B;
  font-family: Helvetica, Arial, sans-serif;
  font-size: 14px;
  margin-left: 2px;
}
</style>
