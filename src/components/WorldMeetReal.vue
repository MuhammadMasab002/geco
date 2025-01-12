<template>
  <section class="world-meet-real-section q-py-xl">
    <div class="container q-py-xl" :class="$q.screen.lt.sm ? 'q-px-md' : 'q-px-xl'">
      <div class="row flex-center q-col-gutter-xl">
        <div class="col-xs-12 col-sm-10 col-md-6">
          <div class="world-real-img">
            <q-img src="/images/cta_img.png" />
          </div>
        </div>
        <div class="col-xs-12 col-sm-10 col-md-6">
          <div class="world-real-text" :class="$q.screen.lt.md ? 'text-center' : 'text-left'">
            <div class="text-layer-img" :style="$q.screen.lt.md ? 'justify-self: center': 'justify-self: start'">
              <q-img src="/images/cta_icon.png" />
            </div>
            <div class="hero_heading text-white text-uppercase text-weight-bolder q-my-none q-py-md"
              :class="$q.screen.xs ? 'text-h4' : 'text-h3'">
              WORLDS MEET
              <span class="text-primary">Real</span>
            </div>
            <p class="text-subtitle1 text-white q-pb-md q-mb-none"
              :style="$q.screen.lt.md ? 'width: 100%;' : 'width: 80%'">
              Compete with 100 player on a remote island for winner known issue where certain strategic
            </p>

            <div>
              <q-img style="width: 300px;" src="/images/title_bar03.png" />
            </div>

            <q-btn flat square :ripple="false" color="black" class="primary-btn add-skew q-ml-xs q-px-lg q-py-md q-mt-xl bg-primary">
              <span class="remove-skew q-px-md text-body1 text-weight-bold">View Schedule</span>
            </q-btn>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  // name: 'ComponentName',
  setup() {
    return {}
  }
}
</script>


<style scoped>
.world-meet-real-section {
  background: url('/images/cta_bg.jpg') no-repeat;
  background-size: cover;
  background-position: center;
  width: 100%;

  .world-real-img {
    width: 100%;
    max-width: 420px;
    height: auto;
    justify-self: center;
  }

  .text-layer-img {
    width: 40px;
    height: 70px;

  }

}
</style>
