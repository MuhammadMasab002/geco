<template>
  <section class="product-corner-section">
    <div class="container q-py-xl" :class="$q.screen.lt.sm ? 'q-px-md' : 'q-px-xl'">
      <div class="row justify-center text-center">
        <div class="col-xs-12 col-sm-9 col-md-7 col-lg-6">
          <div class="q-pt-xl q-pb-lg">
            <h4 class="hero_heading text-white text-uppercase text-h4 q-my-none q-pb-sm"
              :class="$q.screen.lt.sm ? 'text-weight-bold' : 'text-weight-bolder'">
              Gaming Products <span class="text-primary">Corner</span>
            </h4>
            <p class="text-subtitle1 text-white q-pb-md q-mb-none" :class="$q.screen.lt.sm ? 'q-px-md' : 'q-px-xl'">
              Compete with 100 players on a remote island for winner takes showdown known issue where certain skin
              strategic
            </p>
            <q-img style="width: 300px;" src="/images/title_bar03.png" />
          </div>
        </div>
      </div>
      <div class="row justify-center q-py-lg">
        <div class="col-xs-12 col-md-11">
          <Carousel v-bind="config">
            <Slide v-for="card in cardData" :key="card">
              <div class="carousel__item q-ma-md text-left font-oxanium">
                <q-card class="my-card" flat square>
                  <q-img :src="`${card.image}`" />
                  <q-card-section class="q-pa-md">
                    <div class="text-center card-btn">
                      <q-btn flat dense square :ripple="false" class="nav-item add-skew active text-weight-bold q-py-none" >
                        <span class="remove-skew"> {{ card.button }}</span>
                      </q-btn>
                    </div>
                    <div class="card-hover-effect text-h6 text-weight-medium text-white inline-block q-mt-md q-mb-sm">
                      {{ card.name }}
                    </div>
                    <q-card-actions class="q-pa-none">
                      <p class="text-primary text-subtitle1 text-weight-bold q-mb-none">${{ card.price }}</p>
                      <q-space />
                      <q-btn class="custom-btn bg-dark" :ripple="false" size="0.6em" flat icon="shopping_basket"
                        color="primary" />
                    </q-card-actions>
                  </q-card-section>
                </q-card>
              </div>
            </Slide>
          </Carousel>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import '/node_modules/vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

export default {
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
        itemsToShow: 4, // Default for large screens
        breakpoints: {
          1440: {
            itemsToShow: 4, // lg screens and above
          },
          1024: {
            itemsToShow: 3, // md screens below 1024px
          },
          600: {
            itemsToShow: 2, // sm screens below 960px
          },
          0: {
            itemsToShow: 1, // xs screens below 600px
          }
        }
      },
      cardData: [
        {
          id: 1,
          name: 'Men Blue T-shirt',
          button: 'T-shirt',
          price: 29.00,
          image: '/images/s_product_img01.jpg',
        },
        {
          id: 2,
          name: 'Gears 5 xbox Controller',
          button: 'x-box',
          price: 47.00,
          image: '/images/s_product_img02.jpg',
        },
        {
          id: 3,
          name: 'Ge Force rtx 2050',
          button: 'graphices',
          price: 34.00,
          image: '/images/s_product_img03.jpg',
        },
        {
          id: 4,
          name: 'Virtual Reality Smiled',
          button: 'vr-box',
          price: 24.00,
          image: '/images/s_product_img04.jpg',
        },
        {
          id: 5,
          name: 'Ge Force rtx 2050',
          button: 'graphices',
          price: 31.00,
          image: '/images/s_product_img03.jpg',
        },
      ]
    }
  }
};
</script>

<style scoped>
.product-corner-section {
  background-color: #1c181e;
}

.my-card {
  width: 100%;
  box-shadow: 0px 5px 12.09px 0.91px rgba(0, 0, 0, 0.305) !important;
  background-color: #1e1b20;
  /* max-width: 350px; */
}

.carousel__item {
  min-height: 200px;
  width: 100%;
  background-color: var(--brand-color);
  color: #fff;
  font-size: 20px;
  border-radius: 8px;
}

.carousel__slide {
  padding: 1px;
}

.carousel__pagination {
  list-style: none !important;
}

.carousel__pagination-item {
  margin-top: 0 !important;
}

.carousel__slide {
  margin-top: 0 !important;
}

.card-btn {
  margin-top: -35px
}

.card-hover-effect {
  transition: all 0.3s ease;
  text-decoration: none;
  cursor: pointer;

  &:hover {
    color: #ff9900 !important;
  }
}

.custom-btn {
  background-color: #000 !important;
  transition: background-color 0.3s linear, color 0.3s linear;

  &:hover {
    background-color: #ff9900 !important;
    color: #000 !important;
  }
}
</style>
