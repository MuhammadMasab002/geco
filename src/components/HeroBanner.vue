<template>
  <!-- <div class="container"> -->
  <Carousel autopla="4000" wrap-around="true">
    <!-- autoplay="2000" wrap-around="true" -->
    <Slide v-for="slide in 2" :key="slide">
      <div class="carousel__item">
        <div class="main-slider" style="height: 100vh;">

          <div class="slider_circle_img">
            <img src="/images/slider_circle.png" alt="slider_circle" />
          </div>

          <div class="flex hero_text container" :class="$q.screen.lt.md ? 'justify-center' : 'justify-left text-left'">
            <div class="row items-center q-mt-xl"
              :class="$q.screen.lt.md ? 'q-px-none justify-center' : 'q-px-md justify-left'" style="z-index: 10;">
              <div class="col-xs-12 col-sm-9 col-lg-10">
                <h5 class="text-weight-bold text-uppercase q-my-none text-primary"
                  :class="$q.screen.lt.md ? 'text-h6' : 'text-h5'">World Gaming</h5>
                <h1 class="hero_heading text-weight-bolder q-my-none q-py-md"
                  :class="$q.screen.xs ? 'text-h3' : $q.screen.gt.md ? 'text-h1' : 'text-h2'">
                  Create
                  <span class="text-primary">Manage</span> <br>
                  Matches
                </h1>
                <p class="text-subtitle1 q-pb-lg q-mb-none" :class="$q.screen.lt.md ? 'q-pr-none q-px-md' : 'q-pr-xl'"
                  :style="$q.screen.lt.md ? 'width: 100%;' : 'width: 80%'">
                  Find technology or people for digital projects in public sector and Find an individual specialist
                  develope researcher.
                </p>
                <q-btn flat square :ripple="false" color="black"
                  class="primary-btn add-skew q-ml-xs q-mb-lg q-px-lg q-py-md bg-primary q-mr-lg"
                  :class="$q.screen.lt.md ? 'q-mt-md' : 'q-mt-lg'">
                  <span class="remove-skew q-px-md text-body1 text-weight-bold">Read More</span>
                </q-btn>
              </div>
            </div>
            <div class="absolute slider_img1" :class="$q.screen.lt.md ? 'hidden' : 'visible'">
              <img class="img-responsive" :src="'/images/slider_img01.png'" alt="slider_img" sty />
            </div>
            <div class="absolute slider_img2" :class="$q.screen.lt.md ? 'hidden' : 'visible'">
              <img class="img-responsive" :src="'/images/slider_img02.png'" alt="slider_img" sty />
            </div>
          </div>
        </div>
      </div>
    </Slide>

    <!-- <template #addons>
        <Navigation />
        <Pagination />
      </template> -->
  </Carousel>
  <!-- </div> -->
</template>

<script>
import { defineComponent } from 'vue'
import { Carousel, Navigation, Pagination, Slide } from 'vue3-carousel'

import '/node_modules/vue3-carousel/dist/carousel.css'

export default defineComponent({
  name: 'Basic',
  components: {
    Carousel,
    Slide,
    // Pagination,
    Navigation,
  },
  data() {
    return {

    }
  }
})
</script>

<style>
.carousel__item {
  width: 100%;
  min-height: 200px;
  /* background-color: green; */
  color: var(--vc-clr-white);
}

/* .carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border-radius: 50%;
  width: 30px;
  height: 30px;
  cursor: pointer;
  background-color: transparent;
  color: #868484;
  padding: 6px;
  transition: background-color 0.3s, color 0.3s;
}

.carousel__prev:hover,
.carousel__next:hover {
  background-color: rgba(55, 54, 54, 0.9);
  color: #fff;
} */

.main-slider {
  background: url('/images/slider_bg02.jpg') no-repeat;
  background-size: cover;
  width: 100%;
  position: relative;
}

.slider_circle_img {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  /* left: 400px; */
  width: 100%;

}

.slider_circle_img img {
  max-width: 600px;
  margin: 0 auto;
  opacity: 0.2;
  animation: rotateImg 50s linear infinite;
  /* z-index: -2; */
}

/* .slider_circle_img:hover {
  animation-play-state: paused;
} */

.slider_img1 {
  animation-fill-mode: both;
  animation-duration: 1000ms;
  animation-delay: 0.4ms;
  animation-iteration-count: 1;
  opacity: 1;
  animation-name: react-reveal-2;

  bottom: 0;
  right: 50px;
  z-index: 7;

  .img-responsive {
    width: 400px;
  }
}


.slider_img2 {
  animation-fill-mode: both;
  animation-duration: 1000ms;
  animation-delay: 0.4ms;
  animation-iteration-count: 1;
  opacity: 1;
  animation-name: react-reveal-1;

  bottom: 0;
  right: 230px;
  z-index: 1;

  .img-responsive {
    width: 460px;
  }
}

/* animation for circle_circle_img */
@keyframes rotateImg {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}

/* animation for react-reveal */
@keyframes react-reveal-1 {
  from {
    transform: translate3d(-100%, 0px, 0px);
  }

  to {
    transform: none;
  }
}

@keyframes react-reveal-2 {
  from {
    transform: translate3d(100%, 0px, 0px);
  }

  to {
    transform: none;
  }
}

/* responsive styles for mobile -> media queries */

@media screen and (max-width: 1200px) {
  .slider_img1 {
    bottom: 0;
    right: 20px;

    .img-responsive {
      width: 360px;
    }
  }

  .slider_img2 {
    bottom: 0;
    right: 190px;

    .img-responsive {
      width: 400px;
    }
  }
}

@media screen and (max-width: 768px) {
  .slider_circle_img img {
    width: 400px;

  }
}

@media screen and (max-width: 425px) {
  .slider_circle_img img {
    width: 370px;

  }
}
</style>
