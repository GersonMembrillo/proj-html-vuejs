<template>
  <div class="top container">
    <h3 class="text-uppercase text-center fw-bold">Our Events</h3>
    <h4 class="text-center fw-lighter my-4">Chess is fun and we are happy to prove it at our events!</h4>
    <div class="d-flex align-items-center mb-5" v-for="(card, index) in cards" :key="index">
        <div class="col-4">
          <img :src="card.src" :alt="card.title">
        </div>
        <div class="col-8 d-flex align-items-center">
          <div class="p-5">
            <h5 class="fw-bold pb-3">{{ card.title }}</h5>
            <p class="fw-light">{{ card.text }}</p></div>
          <div class="button">
            <button type="button" class="btn btn-warning">Register</button>
          </div>
        </div>
    </div>
  </div>
  <div class="bottom">
    <div class="container">
      <div class="row">
        <div class="col-4">
          <h3 class="fw-bold">Latest News</h3>
          <p class="big-border my-4"></p>
          <button type="button" class="btn btn-outline-dark">View Other Posts</button>
        </div>
        <div class="col-4">
          <img src="../assets/images/mt-2236-blog-img1.jpg" alt="mt-2236-blog-img1.jpg">
          <p class="fw-light pt-2">The most common mistakes when managing personal finances</p>
        </div>
        <div class="col-4">
          <img src="../assets/images/mt-2236-blog-img2.jpg" alt="mt-2236-blog-img2.jpg">
          <p class="fw-light pt-2">Methods of the recruitment</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mainBottomCards } from '../data/data'

export default {
  name: 'MainBottom',
  data() {
    return {
      cards: mainBottomCards
    }
  }
}
</script>

<style lang="scss" scoped>
  img {
    width: 100%;
  }

  .top {
    padding: 75px 0px;
  }

  .bottom {
    padding: 75px 0px 50px 0px;
    background-color: #e8e8e8;

    .big-border {
      border-bottom: 5px solid #ffcd18;
      width: 60px;
    }
  }
</style>
