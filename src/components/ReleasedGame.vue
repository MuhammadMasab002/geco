<template>
  <div class="releasedGame-section">
    <div
      class="container q-py-xl"
      :class="$q.screen.lt.sm ? 'q-px-md' : 'q-px-xl'"
    >
      <div class="row justify-center text-center">
        <div class="col-xs-12 col-sm-9 col-md-7 col-lg-6">
          <div class="q-pt-xl q-pb-lg">
            <h4
              class="hero_heading text-dark text-uppercase text-h4 q-my-none q-pb-sm"
              :class="
                $q.screen.lt.sm ? 'text-weight-bold' : 'text-weight-bolder'
              "
            >
              Released <span class="text-primary">GAMES</span>
            </h4>
            <p
              class="text-subtitle1 q-pb-md q-mb-none"
              :class="$q.screen.lt.sm ? 'q-px-md' : 'q-px-xl'"
            >
              Compete with 100 players on a remote island for winner takes
              showdown known issue where certain skin strategic
            </p>
            <q-img style="width: 300px" src="/images/title_bar02.png" />
          </div>
        </div>
      </div>
      <div class="row q-py-xl">
        <div class="col-xs-12 col-lg-7">
          <Carousel
            class="bg-white"
            id="gallery"
            :items-to-show="1"
            :wrap-around="true"
            v-model="currentSlide"
          >
            <Slide v-for="slide in 4" :key="slide">
              <!-- <div class="carousel__item">{{ slide }}</div> -->
              <div
                class="carousel__item row justify-center"
                :class="$q.screen.lt.sm ? 'q-pa-sm' : 'q-pa-lg'"
              >
                <div class="col-xs-12 col-md-5">
                  <!-- :style="$q.screen.lt.sm ? {'height': 'auto'} : {'height': '450px'}" -->
                  <q-img
                    style="width: 100%; height: 450px"
                    src="/images/released_game_img01.jpg"
                  />
                </div>
                <div class="col-xs-12 col-md-7">
                  <div class="text-left q-py-lg q-pl-md">
                    <div
                      class="text-subtitle1 text-dark text-capitalize text-weight-bold q-pb-md"
                    >
                      Rating:
                      <q-rating
                        v-model="model"
                        max="5"
                        size="1.8em"
                        color="orange-5"
                        icon="star_border"
                        icon-selected="star"
                        icon-half="star_half"
                        no-dimming
                      />
                    </div>
                    <div
                      class="released-game-heading inline-block text-h6 text-dark text-capitalize text-weight-bolder relative-position q-mb-lg"
                    >
                      Call <span class="text-white">of Duty</span>
                    </div>
                    <q-list
                      dense
                      bordered
                      class="text-subtitle1 text-capitalize text-dark text-weight-bold"
                    >
                      <q-item :ripple="false" class="q-mb-sm q-pl-none">
                        <q-item-section class="inline-block">
                          Category:
                          <span
                            class="text-subtitle2 text-grey-7 text-weight-regular q-pl-md"
                            >Vitual Game</span
                          >
                        </q-item-section>
                      </q-item>
                      <q-item :ripple="false" class="q-mb-sm">
                        <q-item-section class="inline-block">
                          Model:
                          <span
                            class="text-subtitle2 text-grey-7 text-weight-regular q-pl-md"
                            >Complete 100 Players</span
                          >
                        </q-item-section>
                      </q-item>
                      <q-item :ripple="false" class="q-mb-sm">
                        <q-item-section class="inline-block">
                          Controller:
                          <span
                            class="text-subtitle2 text-grey-7 text-weight-regular q-pl-md"
                            >Playstation 5, Xbox, PS4</span
                          >
                        </q-item-section>
                      </q-item>
                      <q-item :ripple="false" class="q-mb-sm">
                        <q-item-section class="inline-block">
                          <span
                            class="text-subtitle2 text-grey-7 text-weight-regular"
                            >Complete with 100 players on a remote thats island
                            for winner takes showdown known issue</span
                          >
                        </q-item-section>
                      </q-item>
                    </q-list>
                    <q-btn
                      flat
                      square
                      :ripple="false"
                      color="black"
                      class="primary-btn add-skew bg-primary q-mt-lg q-mb-lg q-ml-md q-px-lg q-py-md"
                    >
                      <span
                        class="remove-skew q-px-md text-body1 text-weight-bold"
                        >Buy Now</span
                      >
                    </q-btn>
                  </div>
                </div>
              </div>
            </Slide>
          </Carousel>
        </div>
        <div
          class="col-xs-12 col-lg-5 overflow-hidden"
          :style="$q.screen.lt.lg ? { height: 'auto' } : { height: '500px' }"
        >
          <!-- <Navigation :current-slide="currentSlide" :slide-change="slideTo" /> -->
          <Carousel
            id="thumbnails"
            :items-to-show="1"
            :wrap-around="true"
            v-model="currentSlide"
            ref="carousel"
          >
            <Slide v-for="slide in 4" :key="slide">
              <div
                class="carousel__item"
                :class="$q.screen.lt.lg ? 'q-gutter-y-md' : 'q-gutter-y-lg'"
                @click="slideTo(slide - 1)"
              >
                <q-img
                  width="100%"
                  :height="$q.screen.lt.lg ? 'auto' : '150px'"
                  src="/images/release_game_nav01.jpg"
                />
                <q-img
                  width="100%"
                  :height="$q.screen.lt.lg ? 'auto' : '150px'"
                  src="/images/release_game_nav02.jpg"
                />
                <q-img
                  width="100%"
                  :height="$q.screen.lt.lg ? 'auto' : '150px'"
                  src="/images/release_game_nav01.jpg"
                />
                <q-img
                  width="100%"
                  :height="$q.screen.lt.lg ? 'auto' : '150px'"
                  src="/images/release_game_nav03.jpg"
                />
              </div>
            </Slide>
          </Carousel>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Slide } from "vue3-carousel";

import "/node_modules/vue3-carousel/dist/carousel.css";

export default defineComponent({
  name: "Gallery",
  components: {
    Carousel,
    Slide,
    Navigation,
  },
  data() {
    return {
      currentSlide: 0,
      model: 3.3,
    };
  },
  methods: {
    slideTo(val) {
      this.currentSlide = val;
    },
  },
});
</script>

<style scoped>
.releasedGame-section {
  background-color: #f6f6f6;
}

.carousel__item {
  background-color: transparent;
  box-shadow: 0px 1px 13px 0px rgba(128, 18, 40, 0.1);
}

.released-game-heading {
  line-height: 50px;

  &::before {
    content: "";
    background: url("/images/released_game_brush.png") no-repeat;
    background-size: cover;
    background-position: right;
    position: absolute;
    top: 0;
    left: -40px;
    right: -50px;
    width: 225px;
    height: 100%;
    z-index: -1;
  }

  @media screen and (max-width: 600px) {
    &::before {
      left: -24px;
    }
  }
}
</style>
