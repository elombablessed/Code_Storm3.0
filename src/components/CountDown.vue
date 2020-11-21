<template>
  <div>
    
    <flip-countdown deadline="2021-2-14 00:00:00" class="white--text"></flip-countdown>
  </div>
</template>

<script>
  import FlipCountdown from 'vue2-flip-countdown'

  export default {
      name:"CountDown",
      components: { FlipCountdown }
  }
</script>