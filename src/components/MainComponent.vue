<template>
  <div class="top">
    <MainTop />
  </div>
  <div class="center">
    <MainCenter />
  </div>
  <div class="bottom">
    <MainBottom />
  </div>
</template>

<script>
import MainTop from './MainTop.vue';
import MainCenter from './MainCenter.vue';
import MainBottom from './MainBottom.vue'

export default {
  name: 'MainComponent',
  components: {
    MainTop,
    MainCenter,
    MainBottom,
  }
}
</script>

<style lang="scss" scoped></style>
