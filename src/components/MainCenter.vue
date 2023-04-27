<template>
  <div class="top container my-5">
    <h3 class="text-uppercase text-center fw-bold">Courses</h3>
    <h4 class="text-center fw-lighter mb-4">To keep up with the constantly rising standards of play</h4>
    <div class="row d-flex">
      <div class="col-4" v-for="(card, index) in cards" :key="index">
        <div class="card h-100">
          <img :src="card.src" class="card-img-top" :alt="card.title">
          <div class="card-body text-center">
            <h5 class="card-title fw-bold">{{card.title}}</h5>
            <p class="card-text fw-light mx-4">{{card.text}}</p>
            <h5 class="card-price fw-bold">{{ card.price }}</h5>
            <a :href="card.href" class="btn btn-warning">View More</a>
          </div>
        </div>
      </div>
    </div>
    <div class="button text-center my-5">
      <button type="button" class="btn btn-outline-dark">View Other Courses</button>
    </div>
  </div>
  <div class="bottom d-flex">
    <div class="container d-flex align-items-center">
      <div class="left">
        <h1 class="text-uppercase text-white fw-bold">take the <span class="text-warning">first step</span></h1>
        <p class="text-white fw-light mb-0">The fascinating world of chess has its doors open for anyone</p>
      </div>
      <div class="right">
        <button type="button" class="btn btn-warning">View More</button>
      </div>
    </div>
  </div>
</template>

<script>
import { mainCenterCards } from '../data/data'

export default {
  name: 'MainCenter',
  data() {
    return {
      cards: mainCenterCards,
    }
  }
}
</script>

<style lang="scss" scoped>

.card {
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
}

.bottom {
  background-image: url('../assets/images/mt-2236-home-bg2.jpg');
  background-size: cover;
  width: 100%;
  height: 240px;
}

.left {
  width: 80%;
}
</style>
