<template>
  <q-page>

    <HeroBanner />
    <ReleasedGame />
    <!-- <newCarousel /> -->
    <JustForGamer />
    <JustFeaturedGame />
    <WorldMeetReal />
    <GamingProductsCorner />
    <LatestArticles />
    <FooterSection />



  </q-page>
</template>

<script>

import HeroBanner from "src/components/HeroBanner.vue";
import ReleasedGame from "src/components/ReleasedGame.vue";
import newCarousel from "src/components/newCarousel.vue";
import JustForGamer from "src/components/JustForGamer.vue";
import JustFeaturedGame from "src/components/JustFeaturedGame.vue";
import WorldMeetReal from "src/components/WorldMeetReal.vue";
import GamingProductsCorner from "src/components/GamingProductsCorner.vue";
import LatestArticles from "src/components/LatestArticles.vue";
import FooterSection from "components/FooterSection.vue";
import carousel from "src/components/carousel.vue";

export default {
  components: {
    HeroBanner,
    ReleasedGame,
    newCarousel,
    JustForGamer,
    JustFeaturedGame,
    WorldMeetReal,
    GamingProductsCorner,
    LatestArticles,
    FooterSection,
  },
  data() {
    return {
    };
  }
}
</script>
