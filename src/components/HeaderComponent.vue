<template>
  <div class="nav text-white">
    <div class="container d-flex justify-content-between">
      <div class="left pt-3">
        <p>6767 Santa Monica Blvd, Los Angeles, CA 90038</p>
        <img src="../assets/images/mt-2236-home-logo.png" alt="">
      </div>
      <div class="right pt-2">
        <div class="d-flex align-items-center justify-content-end">
          <p class="mb-0 me-5">Call Now 123-456-7890</p>
          <button type="button" class="btn btn-light">Donate</button>
        </div>
        <ul class="d-flex list-unstyled">
          <li class="p-2" v-for="(nav, index) in navList" :key="index">
            <a :href="nav.url" class="text-decoration-none" :class="{ 'active': nav.current }">{{ nav.name }}</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
  <div class="hero d-flex align-items-center">
    <div class="container text-white">
      <div class="col-5">
        <span class="badge rounded-pill text-bg-warning text-uppercase mb-3">Welcome</span>
          <h1 class="text-uppercase fw-bold">Academic Chess for <span class="text-warning fst-italic">everyone</span></h1>
          <p class="text-white">We are dedicate to broadening and developing chess as art, recreation, and as a significant element of culture in Northern California.</p>
          <div class="buttons d-flex">
            <button type="button" class="btn btn-warning me-2">Enroll Now</button>
            <button type="button" class="btn btn-outline-light">Learn More</button>
          </div>
      </div>

    </div>
  </div>
</template>

<script>
import { headerList } from '../data/data';

export default {
  name: 'HeaderComponent',
  data() {
    return {
      navList: headerList
    }
  }
}
</script>

<style lang="scss" scoped>

  .hero {
    background-image: url('../assets/images/mt-2236-home-bg1.jpg');
    background-size: cover;
    width: 100%;
    height: 500px;
    position: relative;
  }

  .nav {
    width: 100%;
    height: 80px;
    background-color: rgba(0, 0, 0, 0.5);
    position: absolute;
    z-index: 10;
    font-size: 10px;

    button {
      font-size: 12px;
      padding: 3px 30px;
    }

    a {
    color: white;
    &:hover {
      color: #ffcd18;
    }
  }
  }





</style>
