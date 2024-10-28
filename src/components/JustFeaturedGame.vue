<template>
  <section>
    <div class="container q-py-xl" :class="$q.screen.lt.sm ? 'q-px-md' : 'q-px-xl'">
      <div class="row justify-center text-center">
        <div class="col-xs-12 col-sm-9 col-md-7 col-lg-6">
          <div class="q-pt-xl q-pb-lg">
            <h4 class="hero_heading text-dark text-uppercase text-h4 q-my-none q-pb-sm"
              :class="$q.screen.lt.sm ? 'text-weight-bold' : 'text-weight-bolder'">
              JUST FEATURED <span class="text-primary">GAMES</span>
            </h4>
            <p class="text-subtitle1 q-pb-md q-mb-none" :class="$q.screen.lt.sm ? 'q-px-md' : 'q-px-xl'">
              Compete with 100 players on a remote island for winner takes showdown known issue where certain skin
              strategic
            </p>
            <q-img style="width: 300px;" src="/public/images/title_bar02.png" />
          </div>
        </div>
      </div>
      <div class="row q-col-gutter-lg q-py-xl">
        <div class="col-xs-12 col-sm-6 col-md-4" v-for="card in featuredCard" :key="card">
          <q-card class="my-card">
            <q-img :src="card.imageThumb">
              <div class="text-layer1 absolute-bottom text-left">
                <div class="just-feature-heading text-white text-uppercase text-weight-bold text-h6 q-my-none q-pb-xs">
                  <!-- JUST FEATURED <span class="text-primary">GAMES</span> -->
                  {{ card.title[0] }} <span class="text-primary">{{ card.title[1] }}</span>
                </div>
                <div class="text-body2 text-white q-pb-md q-mb-none">
                  <q-icon class="q-icon" name="notifications" size="1.1rem" color="primary" />
                  {{ card.platforms }}
                </div>
              </div>

              <div class="text-layer2 absolute-full text-center flex flex-center column">
                <div class="text-layer-img">
                  <q-img :src="card.imageIcon" />
                </div>
                <div class="just-feature-heading text-dark text-uppercase text-weight-bolder text-h6 q-my-none q-pb-xs">
                  <!-- JUST FEATURED <span class="text-primary">GAMES</span> -->
                  {{ card.title[0] }} <span class="text-white">{{ card.title[1] }}</span>
                </div>
                <div class="text-body2 text-white q-pb-md q-mb-none">
                  <q-icon class="q-icon" name="notifications" size="1.1rem" color="white" />
                  {{ card.platforms }}
                </div>
              </div>
            </q-img>
          </q-card>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  // name: 'ComponentName',
  setup() {
    return {
      featuredCard: [
        {
          title: ['Just Featured', 'Games'],
          imageThumb: '/images/featured_game_thumb01.jpg',
          imageIcon: '/images/featured_game_icon.png',
          platforms: 'PlayStation 5, Xbox',
        },
        {
          title: ['Just Featured', 'Games'],
          imageThumb: '/images/featured_game_thumb02.jpg',
          imageIcon: '/images/featured_game_icon.png',
          platforms: 'PlayStation 5, Xbox',
        },
        {
          title: ['Just Featured', 'Games'],
          imageThumb: '/images/featured_game_thumb03.jpg',
          imageIcon: '/images/featured_game_icon.png',
          platforms: 'PlayStation 5, Xbox',
        },
        {
          title: ['Just Featured', 'Games'],
          imageThumb: '/images/featured_game_thumb04.jpg',
          imageIcon: '/images/featured_game_icon.png',
          platforms: 'PlayStation 5, Xbox',
        },
        {
          title: ['Just Featured', 'Games'],
          imageThumb: '/images/featured_game_thumb05.jpg',
          imageIcon: '/images/featured_game_icon.png',
          platforms: 'PlayStation 5, Xbox',
        },
        {
          title: ['Just Featured', 'Games'],
          imageThumb: '/images/featured_game_thumb06.jpg',
          imageIcon: '/images/title_bar06.png',
          platforms: 'PlayStation 5, Xbox',
        },
      ]
    }
  }
}
</script>

<style scoped>
.my-card {
  width: 100%;

  .text-layer1 {
    /* transition: opacity 0.5s ease-in-out, visibility 0.5s ease-in-out; */
    transition: 0.3s linear;
    opacity: 1;
    visibility: visible;
    background-color: transparent !important;

  }

  .text-layer2 {
    transition: 0.3s linear;
    opacity: 0;
    visibility: hidden;
  }

  .text-layer-img {
    width: 40px;
    height: 90px;

  }

  &:hover {
    .text-layer1 {
      opacity: 0;
      visibility: hidden;
    }

    .text-layer2 {
      opacity: 0.8;
      visibility: visible;
      /* width: 100%; */
      text-align: center;
      vertical-align: middle;
      background-color: #d8a533 !important;
    }

    .just-feature-heading {
      color: #000 !important;
    }

    .just-feature-heading span {
      color: #fff !important;
    }

    .just-feature-heading .q-icon {
      color: #fff !important;
    }
  }
}
</style>
