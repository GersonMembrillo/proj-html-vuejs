<template>
  <div class="top">
    <MainTopCard />
  </div>
  <div class="center">
    <MainCenterCard />
  </div>
  <div class="bottom">
    <MainBottomCard />
  </div>
</template>

<script>
import MainTopCard from './MainTopCard.vue';
import MainCenterCard from './MainCenterCard.vue';
import MainBottomCard from './MainBottomCard.vue'

export default {
  name: 'MainComponent',
  components: {
    MainTopCard,
    MainCenterCard,
    MainBottomCard,
  }
}
</script>

<style lang="scss" scoped></style>
