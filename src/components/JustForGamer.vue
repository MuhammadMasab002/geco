<template>
  <section class="just-gamers-area q-py-xl">
    <div class="container q-py-xl q-px-xl">
      <div class="row">
        <div class="col-xs-12 col-sm-10 col-md-6 col-lg-5">
          <div class="q-pb-lg">
            <h4 class="hero_heading text-white text-uppercase text-h4 q-my-none q-pb-sm"
              :class="$q.screen.lt.sm ? 'text-weight-bold' : 'text-weight-bolder'">
              Just For <span class="text-primary">Gamers</span>
            </h4>
            <p class="text-subtitle1 text-grey-4 q-pb-md q-mb-none">
              Compete with 100 player on a remote island for winner known issue where certain strategic
            </p>
            <q-img style="width: 300px;" src="/images/title_bar03.png" />
          </div>
          <div class="just-gamer-list q-mt-xl">
            <q-list dense class="q-gutter-y-lg">
              <q-item class="gamer-item" :ripple="false" v-for="list in gamerList" :key="list">
                <q-item-label class="icon-wrapper q-mr-md" >
                  <img :src="list.icon" class="gamer-icon" />
                </q-item-label>
                <q-item-label class="text-section">
                  <h5 class="text-h6 text-weight-bold text-white gamer-title q-my-none q-pb-xs">{{ list.title }}</h5>
                  <p class="text-subtitle1 text-grey-4 gamer-description">{{ list.description }}</p>
                </q-item-label>
              </q-item>
            </q-list>
          </div>
        </div>
        <div class="col-xs-12 col-md-6 col-lg-7" v-if="$q.screen.gt.sm">
          <div class="just-gamer-img absolute-left flex flex-center">
            <q-img src="/images/just_gamers_img.png" />
          </div>
          <div class="just-gamer-circle-shapes">
            <img class="line-shape" src="/images/gamers_circle_line.png" />
            <img class="circle-shape" src="/images/gamers_circle_shape.png" />
          </div>
          <q-img v-if="$q.screen.gt.md" class="gamer-chart" src="/images/just_gamers_chart.png" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  setup() {
    return {
      gamerList: [
        {
          title: 'VR Development',
          description:
            'See how well critics rating new video game release with 100 players',
          icon: '/images/gamer_list_icon01.png'
        },
        {
          title: 'Design & Strategy',
          description:
            'Village and the subline of her own road, the Line Lane. Pityful a rethoric question',
          icon: '/images/gamer_list_icon02.png'
        },
        {
          title: 'Jungle Pharaoh',
          description:
            'Village and the subline of her own road, the Line Lane. Pityful a rethoric question',
          icon: '/images/gamer_list_icon03.png'
        }
      ]
    }
  }
}
</script>

<style scoped>
.just-gamers-area {
  position: relative;

  &::before,
  &::after {
    content: '';
    position: absolute;
    /* left: 50%; */
    left: 0;
    right: 0;
    margin: 0 auto;
    width: 420px;
    height: 150px;
    /* transform: translateX(-50%); */
    z-index: 1;

  }

  &::before {
    background: url('/images/gamers_bg_conve01.png') no-repeat;
    background-size: cover;
    background-position: center;
    top: -1px;
  }

  &::after {
    background: url('/images/gamers_bg_conve02.png') no-repeat;
    background-size: cover;
    background-position: center;
    bottom: -1px;
    /* background-color: rgba(156, 43, 43, 0.8); */
    z-index: 1;
  }

  @media screen and (max-width: 1400px) {

    &::before,
    &::after {
      left: auto;
      right: 200px;
      margin: unset;
    }
  }

  @media screen and (max-width: 1024px) {

    &::before,
    &::after {
      display: none;
    }
  }

  .just-gamer-img {
    width: 230px;
    left: 52%;
    transform: translate(-50%);
    z-index: 2;
  }

  @media screen and (max-width: 1400px) {
    .just-gamer-img {
       left: 60%;
       transform: translateX(0);
    }
  }

}

.just-gamers-area {
  background: url('/images/just_gamer_bg.jpg') no-repeat;
  background-position: center;
  background-size: cover;

  .gamer-item {
    display: flex;
    align-items: center;
    padding: 0 !important;

    .icon-wrapper {
      display: flex;
      justify-content: center;
      align-items: center;
      min-width: 100px;
      min-height: 100px;
      background: url('/images/gamer_list_icon_bg.jpg');
      border: 6px solid #333240;
      transition: 0.3s linear;

    }

    &:hover .icon-wrapper {
      border-color: #e9a301;
    }

    .gamer-title {
      margin: 0;
      font-size: 1.1rem;
      font-weight: bold;
    }

    .gamer-description {
      margin: 0;
      font-size: 0.9rem;
    }
  }

  .just-gamer-circle-shapes {
    position: absolute;
    top: 0;
    left: 50%;
    right: 0;
    bottom: 0;
    height: 100%;
    z-index: 1;

    .line-shape {
      position: absolute;
      left: -5px;
      top: 48%;
      padding: 50px;
      width: 280px;
      height: 210px;
    }

    .circle-shape {
      width: 150px;
      height: 150px;
      position: absolute;
      left: 145px;
      top: 59%;
      animation: rotateImg 50s linear infinite;
    }

  }

  @media screen and (max-width: 1400px) {
    .just-gamer-circle-shapes {
       left: 65%;
    }
  }

  .gamer-chart {
    position: absolute;
    top: 90px;
    right: 150px;
    /* width: 100%; */
    max-width: 350px;
    margin: 0 auto;
  }
}

@keyframes rotateImg {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}
</style>
