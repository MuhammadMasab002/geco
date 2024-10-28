<template>
  <q-page class="">
    <div class="row justify-center">
      <div class="col-10">
        <Carousel v-bind="config">
          <Slide v-for="slide in 5" :key="slide" style="background-color: red;">
            <div class="carousel__item bg-blue text-blue q-ma-md">
              <q-card class="my-card">
                <img src="https://cdn.quasar.dev/img/mountains.jpg">
                <q-card-section>
                  <div class="text-h6">Our Changing Planet</div>
                  <div class="text-subtitle2">by John Doe</div>
                </q-card-section>

                <q-card-section class="q-pt-none">
                  {{ lorem }}
                </q-card-section>
              </q-card>
            </div>
          </Slide>

          <!-- <template #addons>
            <Navigation />
          </template> -->
        </Carousel>
      </div>
    </div>
  </q-page>
</template>

<script>
import '/node_modules/vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'


import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  data() {
    return {
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
      config: {
        effect: 'fade',
        speed: 2000,
        itemsToShow: 4,
        snapAlign: 'start',
        wrapAround: true,
        autoplay: 2000,
        // autoplayHoverPause: true,
        pauseAutoplayOnHover: true,
        responsive: {
          324: {
            items: 1,
            align: "start",
          },
          576: {
            items: 2,
            align: "start",
          },
          768: {
            items: 3,
            align: "start",
          },
          992: {
            items: 4,
            align: "start",
          },
          1200: {
            items: 5,
            align: "start",
          }
        }
      }
    }
  }
});
</script>
<style>
.my-card {
  width: 100%;
  /* max-width: 250px */
}

</style>
