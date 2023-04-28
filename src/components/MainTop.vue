<template>
    <div class="top container">
      <h3 class="text-uppercase text-center fw-bold">Our Services</h3>
      <h4 class="text-center fw-lighter my-4">We make your child happy day after day</h4>
      <div class="row">
        <div class="col-4">
          <h5>Chess Education</h5>
          <h6>Popular education for your child and your</h6>
          <p class="fw-light">Teachers and parents around the world know that chess is not a simple game. It is a great learning tool that will help build your child's executive function skills.</p>
          <ul>
            <li class="py-2" v-for="index in proList" :key="index"><span class="ps-2">{{ index }}</span></li>
          </ul>
          <button type="button" class="btn btn-warning">Learn More</button>
        </div>
        <div class="col-8 d-flex justify-content-between flex-wrap">
          <div class="card" v-for="(service,index) in services" :key="index">
              <img :src="service.src" :alt="service.title" class="card-img">
              <p class="card-title fw-bold my-3">{{ service.title }}</p>
              <p class="card-text fw-light">{{ service.text }}</p>
          </div>
        </div>
      </div>
    </div>
    <div class="bottom">
      <div class="up">
        <div class="row">
          <div class="col-3 px-0" v-for="index in images" :key="index">
            <img :src="index">
          </div>
        </div>
      </div>
      <div class="down bg-warning">
        <div class="container d-flex align-items-center">
          <div class="d-flex left">
            <img src="../assets/images/mt-2236-home-icon5.png" alt="mt-2236-home-icon5.png" class="m-4">
            <div class="middle-text ms-4">
              <h3 class="text-uppercase fw-bold">play & learn</h3>
              <p class="mb-0 fw-light">Take a look into our day to day life here at Chess School</p>
            </div>
          </div>
          <div class="right">
            <button type="button" class="btn btn-outline-dark">Learn More</button>
          </div>

        </div>
      </div>
    </div>
</template>

<script>
import { mainTopList } from '../data/data';
import { mainTopCards } from '../data/data';
import { mainTopImages } from '../data/data';

export default {
  name: 'MainTop',
  data() {
    return {
      proList: mainTopList,
      services: mainTopCards,
      images: mainTopImages,
    }
  }
}
</script>

<style lang="scss" scoped>
  .top {
    padding: 75px 0px;
    ul{
    list-style-image: url('../assets/images/mt-2236-home-icon-bullet.png');
    }
  }



  .card {
    width: 48%;
    border: none;

    .card-img {
      width: 50px;
      height: 50px;
    }
  }

  .bottom {
    .col-3 img {
      width: 100%;
      height: auto;
    }

    .middle-text {
      margin: auto;
    }

    .down {
      img {
      width: 70px;
      height: auto;
    }
    }
  }

  .left {
    width: 80%;
  }
</style>
