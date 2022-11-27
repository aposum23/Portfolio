<template>
  <div class="lightning-comp">
    <svg width="160" height="420">
      <linearGradient id="linear-gradient">
        <stop offset="0%" stop-color="#53A620"/>
        <stop offset="100%" stop-color="#caeb10"/>
      </linearGradient>
      <path class="lightning" d="M125,40 Q160,0 150,30 150,30 90,190 Q80,220 120,230 Q160,250 30,400 Q0,420 45,290 Q50,270 30,250 Q0,210 30,160 z" fill="url(#linear-gradient)" stroke="#fff" stroke-width="3"/>
    </svg>
  </div>
</template>

<script>
export default {
  name: 'LightningComp'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
svg {
  margin: 0px 10em;
}
.lightning-comp {
  width: 50%;
  height: 500px;
}

.lightning {
  stroke-dasharray: 500;
  animation: dash 5s ease-in;
  animation-iteration-count: infinite;
}

@keyframes dash {
  to {
    stroke-dashoffset: 1000;
  }
}
</style>
