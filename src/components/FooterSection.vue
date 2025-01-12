<template>
  <div class="footer-section q-mt-xl">
    <div class="container q-py-xl" :class="$q.screen.lt.sm ? 'q-px-md' : 'q-px-xl'">
      <div class="row justify-center items-center">
        <div class="col-xs-12 col-md-11">
          <div class="q-py-xl newsletter-main">
            <div class="row items-center"
              :class="$q.screen.lt.md ? 'justify-center q-gutter-y-md q-px-lg' : 'justify-between q-px-xl'">
              <div class="col-xs-12 col-md-4">
                <div class="font-oxanium text-h5 text-uppercase text-weight-bolder text-white"
                  :class="$q.screen.lt.md ? 'text-center' : 'text-end'">
                  our <span class="text-primary">Newsletter</span>
                </div>
              </div>
              <div class="col-xs-12 col-md-8">
                <q-form>
                  <div class="row input-group items-center"
                    :class="$q.screen.lt.md ? 'justify-center q-px-none q-gutter-y-md' : $q.screen.lt.lg ? 'justify-end q-px-sm' : 'justify-end q-px-md'">
                    <q-input standout class="add-skew custom-input inline-block text-white text-subtitle1 text-weight-bold" color="primary"
                       square v-model="email" placeholder="Enter your email..."
                      :style="$q.screen.lt.sm ? 'width: 310px' : 'width: 60%'">
                      <template v-slot:prepend>
                        <q-icon class="remove-skew" name="fa-regular fa-envelope" color="primary" />
                      </template>
                    </q-input>
                    <q-btn flat square :ripple="false" color="black"
                      class="add-skew bg-primary q-ml-md q-px-md q-py-md">
                      <span class="remove-skew q-px-md text-body1 text-weight-bold">
                        Subscribe
                        <q-icon name="fa fa-paper-plane" size="18px" class="q-ml-sm q-mb-xs" />
                      </span>
                    </q-btn>

                  </div>
                </q-form>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="row justify-center q-mt-xl">
        <div class="col-xs-12 col-sm-11">
          <div padding class="q-mx-auto row justify-betwee">

            <div class="col-xs-12 col-sm-10 col-md-6 col-lg-4 text-white">
              <div class="footer-logo flex items-center q-mb-lg">
                <q-icon name="camera" size="46px" color="orange" />
                <span class="font-oxanium text-h4 text-weight-bolder q-ml-sm">Geco</span>
              </div>
              <p class="text-subtitle1 text-grey-5 text-weight-medium q-mb-none">
                Gemas marketplace the relase etras thats sheets continig passag.
              </p>
              <div class="text-subtitle1 text-grey-5 text-weight-medium q-mb-none q-mt-md">
                <p class="q-mb-none q-pb-sm">
                  <q-icon class="q-mr-sm" color="primary" name="place" size="18px" />
                  Address : PO Box W75 Street Ian West new queens
                </p>
                <p class="q-mb-none q-pb-sm">
                  <q-icon class="q-mr-sm" color="primary" name="phone" size="18px" />
                  Phone : +24 1245 654 235
                </p>
                <p class="q-mb-none q-pb-sm">
                  <q-icon class="q-mr-sm" color="primary" name="email" size="18px" />
                  Email : info@example.com
                </p>
              </div>
            </div>

            <div class="col-xs-12 col-sm-6 col-md-3 col-lg-2 " :class="$q.screen.lt.md ? 'q-pl-none' : 'q-pl-lg'">
              <h5 class="font-oxanium text-h5 text-weight-bold text-white q-my-none q-pb-lg"
                :class="$q.screen.lt.md ? 'q-pt-lg' : 'q-pt-sm'">Products</h5>
              <q-list dense bordered padding="none" class="rounded-border text-grey-5 q-pr-sm">
                <q-item clickable :ripple="false" class="q-mb-sm footer-item no-hover">
                  <q-item-section>
                    <q-item-label>Graphics (26)</q-item-label>
                  </q-item-section>
                </q-item>
                <q-item clickable :ripple="false" class="bg- q-mb-sm footer-item no-hover">
                  <q-item-section>
                    <q-item-label>Backgrounds (11)</q-item-label>
                  </q-item-section>
                </q-item>
                <q-item clickable :ripple="false" class="bg- q-mb-sm footer-item no-hover">
                  <q-item-section>
                    <q-item-label>Fonts (9)</q-item-label>
                  </q-item-section>
                </q-item>
                <q-item clickable :ripple="false" class="bg- q-mb-sm footer-item no-hover">
                  <q-item-section>
                    <q-item-label>Music (3)</q-item-label>
                  </q-item-section>
                </q-item>
                <q-item clickable :ripple="false" class="bg- q-mb-sm footer-item no-hover">
                  <q-item-section>
                    <q-item-label>Photography (3)</q-item-label>
                  </q-item-section>
                </q-item>
              </q-list>
            </div>
            <div class="col-xs-12 col-sm-6 col-md-3 col-lg-2 " :class="$q.screen.lt.md ? 'q-pl-none' : 'q-pl-lg'">
              <h5 class="font-oxanium text-h5 text-weight-bold text-white q-my-none q-pb-lg"
                :class="$q.screen.lt.md ? 'q-pt-lg' : 'q-pt-sm'">Need Help?</h5>
              <q-list dense bordered padding="none" class="rounded-border text-grey-5 q-pr-sm">
                <q-item clickable :ripple="false" class="q-mb-sm footer-item no-hover">
                  <q-item-section>
                    <q-item-label>Terms & Conditions</q-item-label>
                  </q-item-section>
                </q-item>
                <q-item clickable :ripple="false" class="bg- q-mb-sm footer-item no-hover">
                  <q-item-section>
                    <q-item-label>Privacy Policy</q-item-label>
                  </q-item-section>
                </q-item>
                <q-item clickable :ripple="false" class="bg- q-mb-sm footer-item no-hover">
                  <q-item-section>
                    <q-item-label>Refund Policy</q-item-label>
                  </q-item-section>
                </q-item>
                <q-item clickable :ripple="false" class="bg- q-mb-sm footer-item no-hover">
                  <q-item-section>
                    <q-item-label>Affiliate</q-item-label>
                  </q-item-section>
                </q-item>
                <q-item clickable :ripple="false" class="bg- q-mb-sm footer-item no-hover">
                  <q-item-section>
                    <q-item-label>FAQUse Cases</q-item-label>
                  </q-item-section>
                </q-item>
              </q-list>
            </div>

            <div class="col-xs-12 col-sm-8 col-md-4 col-lg-4 text-white">
              <h5 class="font-oxanium text-h5 text-weight-bold text-white q-my-none q-pb-lg"
                :class="$q.screen.lt.lg ? 'q-pt-lg' : 'q-pt-sm'">Follow us</h5>
              <div class="footer-social-links q-mb-md">
                <q-btn flat dense icon="fa-brands fa-facebook-f" class="text-body2 bg-indigo-13 text-white q-mr-sm" />
                <q-btn flat dense icon="fa-brands fa-twitter" class="text-body2 bg-light-blue-5 text-white q-mr-sm" />
                <q-btn flat dense icon="fa-brands fa-pinterest-p" class="text-body2 bg-red-9 text-white q-mr-sm" />
                <q-btn flat dense icon="fa-brands fa-linkedin-in" class="text-body2 bg-indigo-8 text-white" />
              </div>
              <h5 class="font-oxanium text-h5 text-weight-bold text-white q-my-none q-pb-lg q-pt-lg">Newsletter Sign Up
              </h5>
              <q-input standout square v-model="text" placeholder="Enter your email"
                class="footer-input custom-input text-subtitle2 text-white">
                <template #append>
                  <q-icon name="fa-solid fa-rocket" class="text-dark bg-orange q-pa-md" />
                </template>
              </q-input>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row bg-black">
      <div class="col-xs-12">
        <div class="container" :class="$q.screen.lt.sm ? 'q-px-md' : 'q-px-lg'">
          <div class="row justify-center q-py-sm">
            <div class="col-xs-12 col-sm-11">
              <q-bar dense class="text-white q-py-lg" :class="$q.screen.lt.md ? 'justify-center' : 'justify-between'">
                <div class="text-subtitle1 text-weight-medium text-grey-6 text-center">
                  Copyright © 2022 <span class="text-primary">Geco</span> All Rights Reserved.
                </div>
                <div class="gt-sm">
                  <q-img src="/images/card_img.png" width="380px" height="100%" />
                </div>
              </q-bar>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  // name: 'ComponentName',
  data() {
    return {
      text: '',
      email: ''
    }
  }
}
</script>

<style scoped lang="scss">
/* .footer-container {
  background-color: #1a1a2e;
} */

.footer-section {
  background: url('/public/images/footer_bg.jpg') no-repeat;
  background-size: cover;
  background-position: center;
}

.newsletter-main {
  border-radius: 100px;
  margin-top: -110px;
  background-color: rgb(25, 14, 34);

  @media screen and (max-width: 768px) {
    border-radius: 70px;
    margin-top: -100px;
  }
}

.custom-input {
  color: white !important;
  background-color: #24182d;

  & ::placeholder {
    color: white;
    opacity: 1
  }
}

:deep(.no-hover:hover>.q-focus-helper) {
  background-color: transparent !important;
  opacity: 0 !important;
}

.footer-item {
  padding-left: 0 !important;
  transition: .3s ease-in-out;

  &:hover {
    /* background-color: transparent !important; */
    color: #ffcc00;
    padding-left: 4px !important;
  }
}

.footer-social-links .q-btn {
  width: 40px;
  height: 40px;
}
</style>
