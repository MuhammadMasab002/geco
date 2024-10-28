<template>
  <q-layout class="bg-transparent"view="hHh lpR fFf">

    <navbar />

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import Navbar from 'components/Navbar.vue'

export default {
  components: {
    Navbar,
  }
}
</script>









<!-- <template>
  <q-layout>
    <q-header elevated>
      <q-toolbar class="bg-red text-white">

        <q-img src="/images/logo.png" alt="Logo" style="height: auto; width: 150px;" />

        <q-space />

        <q-tabs
          class="q-ml-md text-black text-weight-bolder"
          active-bg-color="yellow-8"
          indicator-color="yellow-8"
          v-model="tab"
        >
          <q-tab name="home" label="HOME"/>
          <q-tab name="pages" label="PAGES" />
          <q-tab name="overview" label="OVERVIEW" />
          <q-tab name="community" label="COMMUNITY" />
          <q-tab name="store" label="STORE" />
          <q-tab name="blog" label="BLOG" />
          <q-tab name="contact" label="CONTACT" />
        </q-tabs>

        <q-btn-dropdown
          flat
          label="Home"
          square
          color="black"
          no-icon
        >
          <q-list class="dropdown-list-square">
            <q-item clickable v-close-popup>
              <q-item-section>
                <q-item-label>Home one</q-item-label>
              </q-item-section>
            </q-item>

            <q-item clickable v-close-popup>
              <q-item-section>
                <q-item-label>Home two</q-item-label>
              </q-item-section>
            </q-item>

            <q-item clickable v-close-popup>
              <q-item-section>
                <q-item-label>Home three</q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-btn-dropdown>

        <q-btn flat icon="shopping_cart" class="q-mr-sm text-white">
          <q-badge color="yellow-8" floating>0</q-badge>
        </q-btn>

        <q-btn flat icon="search" class="text-white bg-black" push />

      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from 'vue'

const tab = ref('home')
</script>

<style scoped>
.q-header {
  height: 100px;
}

.q-toolbar {
  padding: 0 16px;
}

.dropdown-list-square {
  border-radius: 0;
}

.q-btn-dropdown {
  border-radius: 0;
}

.q-item {
  border-radius: 0 !important;
}

.q-btn {
  border-radius: 0;
}

.q-badge {
  font-size: 12px;
}
</style> -->
