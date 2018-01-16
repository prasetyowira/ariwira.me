<template>
  <div class="home">
    <wira-terminal />
  </div>
</template>

<script>
import Terminal from '@/components/UI/Terminal';

export default {
  name: "wira-home",
  components: {
    "wira-terminal": Terminal,
  }
}
</script>

<style lang='scss' scoped>
  .home{
    padding: 100px;
  }
</style>
