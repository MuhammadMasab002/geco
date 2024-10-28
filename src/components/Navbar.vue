<template>
  <!-- <q-header class="q-px-xl bg-red"> -->
  <div class="row bg-black ">
    <div class="col-xs-12">
      <div class="container" :class="$q.screen.lt.sm ? 'q-px-md' : ''">
        <q-bar dens class="bg-transparent text-white">
          <div class="text-caption text-grey-4 text-weight-light ">Exclusive Black Friday ! Offer</div>
          <q-icon name="email" />
          <q-space />
          <q-icon class="text-grey-4 q-mx-sm" size="0.7em" name="fa-brands fa-facebook-f" />
          <q-icon class="text-grey-4 q-mx-sm" size="0.7em" name="fa-brands fa-twitter" />
          <q-icon class="text-grey-4 q-mx-sm" size="0.7em" name="fa-brands fa-pinterest-p" />
          <q-icon class="text-grey-4 q-mx-md" size="0.7em" name="fa-brands fa-linkedin-in" />
          <span class="text-primary q-ml-md q-mr-sm"> | </span>
          <q-icon class="q-ml-sm" size="0.7em" name="fa-regular fa-envelope" color="primary" />
          <div class="text-caption text-grey-4 text-weight-light">info@gmail.com</div>
        </q-bar>
      </div>
    </div>
  </div>
  <div class="container relative-position">
    <q-toolbar class="bg-nav text-white q-py-md q-px-lg q-mt-md absolute"
      style=" border-bottom-left-radius: 10px; border-bottom-right-radius: 10px; z-index: 888;">

      <!-- Logo -->
      <q-img src="/images/logo.png" alt="Logo" class="logo" height="40px" width="140px" />

      <q-space />

      <div v-if="$q.screen.gt.md">

        <q-btn v-for="item in navbarItems" :key="item" flat square :ripple="false"
          :class="`q-ml-md text-weight-bold nav-item add-skew q-btn-dropdown ${item.className}`">

          <span class="remove-skew">{{ item.label }}</span>

          <q-menu class="text-white text-uppercase" style="border-radius: 0; background: #1c1421;">
            <q-list v-if="item.drowpData" class="q-py-md">
              <q-item class="q-py-sm q-pl-lg q-pr-xl dropItem" clickable :ripple="false" dense
                v-for="option in item.drowpData" :key="item">
                <q-item-label class="q-pr-xl">{{ option.label }}

                </q-item-label>
              </q-item>
            </q-list>
          </q-menu>
        </q-btn>
      </div>

      <!-- Cart Icon -->
      <div v-if="$q.screen.gt.xs">
        <q-btn flat icon="shopping_cart" :ripple="false" class="q-mr-sm text-white">
          <q-badge class="q-p-sm text-black text-subtitle2" dense color="primary" rounded floating>0</q-badge>
        </q-btn>

        <!-- Search Icon -->
        <q-btn flat :ripple="false" icon="search" color="primary" class="q-mx-md q-py-md bg-black" />
      </div>

      <q-btn class="menu-icon" v-if="$q.screen.lt.lg" flat @click="drawerRight = !drawerRight" round dense
        icon="menu" />
    </q-toolbar>
  </div>
  <!-- </q-header> -->


  <q-drawer side="right" v-model="drawerRight" overlay bordered :width="200" :breakpoint="500" class="text-white"
    :class="$q.dark.isActive ? 'bg-dark' : 'bg-dark'">
    <div class="text-right q-pt-md q-pr-md">
      <q-btn flat @click="drawerRight = !drawerRight" round dense icon="close" />
    </div>
    <div class="q-pa-sm">
      <q-list dense bordered padding class="rounded-borders">
        <q-item clickable v-ripple v-for="item in navbarItems" :key="item.id">
          <q-item-section class="dropItem">
            {{ item.label }}
          </q-item-section>
        </q-item>
      </q-list>
    </div>
  </q-drawer>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      drawerRight: false,
      navbarItems: [
        {
          label: "Home", className: "active", drowpData: [
            { label: "Home One", },
            { label: "Home Two", },
            { label: "Home Three", },
            { label: "Home Four", },
            { label: "Home Five", },
            { label: "Home Six", },
            { label: "Home Seven", },
          ]
        },
        { label: "Pages", drowpData: [
            { label: "Page One", },
            { label: "Page Two", },
            { label: "Page Three", },
          ] },
        { label: "Overview" },
        { label: "Community" },
        { label: "Store" },
        { label: "Blog", drowpData: [
            { label: "Blog One", },
            { label: "Blog Two", },
            { label: "Blog Three", },
          ] },
        { label: "Contact" },
      ],
    }
  },
}
</script>

<style scoped>
.bg-nav {
  background: url('/public/images/header_bg.jpg') no-repeat;
  background-size: cover;
  background-position: center;
  transition: 0.3s ease;
}
.menu-icon {
  font-size: 16px;
}

.dropItem {
  transition: 0.3s ease;

  &:hover {
    color: #ff9900;

  }
}
</style>
