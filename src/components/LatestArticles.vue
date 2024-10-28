<template>
  <section>
    <div class="container q-py-xl" :class="$q.screen.lt.sm ? 'q-px-md' : 'q-px-xl'">
      <div class="row justify-center text-center">
        <div class="col-xs-12 col-sm-9 col-md-7 col-lg-6">
          <div class="q-pt-xl q-pb-lg">
            <div class="hero_heading font-oxanium text-dark text-uppercase text-h4 q-pb-sm"
              :class="$q.screen.lt.sm ? 'text-weight-bold' : 'text-weight-bolder'">
              Latest News <span class="text-primary">Articles</span>
            </div>
            <p class="text-subtitle1 q-pb-md q-mb-none" :class="$q.screen.lt.sm ? 'q-px-md' : 'q-px-xl'">
              Compete with 100 players on a remote island for winner takes showdown known issue where certain skin
              strategic
            </p>
            <q-img style="width: 300px;" src="/public/images/title_bar02.png" />
          </div>
        </div>
      </div>
      <div class="row justify-center q-col-gutter-lg q-py-xl">
        <div class="co-xs-12 col-md-11">
          <div class="row justify-center q-col-gutter-lg q-px-md">
            <div class="col-xs-12 col-sm-6 col-md-4" v-for="card in articleData" :key="card">
              <q-card class="my-card no-shadow" square>

                <!-- <div class="q-pa-xs"> -->
                <q-img class="article-card-img" :src="`${card.image}`" />
                <!-- </div> -->
                <q-card-section class="q-px-none">
                  <div class="card-hover-effect font-oxanium text-h6 text-weight-bolder text-uppercase">
                    {{ card.title }}
                  </div>
                  <div class="text-subtitle2 text-italic text-grey-7">
                    <span class="q-pr-md"><q-icon name="access_time" color="primary" size="1.2em" class="q-pr-sm" />
                      {{ card.date }}</span>
                    <span><q-icon name="local_offer" color="primary" size="1.2em" class="q-pr-sm" />
                      {{ card.category }}</span>
                  </div>
                </q-card-section>

                <q-card-section class="q-px-none">
                  <div class="text-subtitle1 text-grey-7 text-weight-medium q-pt-none">{{ card.content }}</div>
                </q-card-section>
              </q-card>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  // name: 'ComponentName',
  data() {
    return {
      articleData: [
        {
          title: 'Shooter action video game',
          image: '/images/s_blog_thumb01.jpg',
          date: 'July 4, 2023',
          category: 'Shooter',
          content: 'Compete with 100 players on a remote island for winner takes showdown known for issue where certain skin strategic [...]'
        },
        {
          title: 'multiplayer environments',
          image: '/images/s_blog_thumb02.jpg',
          date: 'July 4, 2023',
          category: 'Shooter',
          content: 'Compete with 100 players on a remote island for winner takes showdown known for issue where certain skin strategic [...]'
        },
        {
          title: 'Bullet Force Multiplayer',
          image: '/images/s_blog_thumb03.jpg',
          date: 'July 4, 2023',
          category: 'Shooter',
          content: 'Compete with 100 players on a remote island for winner takes showdown known for issue where certain skin strategic [...]'
        },
      ]
    }
  }
}
</script>


<style scoped>
.article-card-img {
  cursor: pointer;
  padding: 5px;
  box-shadow: rgba(106, 106, 106, 0.24) 1px 3px 8px !important;
}

.card-hover-effect {
  transition: all 0.3s ease;
  text-decoration: none;
  cursor: pointer;

  &:hover {
    color: #ff9900 !important;
  }
}
</style>
