<template>
  <main>
    <v-navigation-drawer height="530" width="100%" color="rgba(0, 0, 0, 0.9)" disable-resize-watcher
      v-model="sideNav.model" :clipped="$vuetify.breakpoint.lgAndUp" app>
      <div style="position: relative">
        <v-icon style="position: absolute; right: 10px; top: 10px;" @click="sideNav.model = false"
          color="white">mdi-close-circle</v-icon>
      </div>

      <v-sheet tile color="transparent" class="py-3 mt-12 mb-5 d-flex justify-center">
        <nuxt-link to="/">
          <img src="/images/rendezvous-logo.png" width="170" class="mx-auto">
        </nuxt-link>
      </v-sheet>

      <v-list shaped dense>
        <template>
          <v-list-item   v-for="item in items" color="cta" dark nuxt :to="item.to" :key="item.text">
            <v-list-item-action>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>
                {{ item.text }}
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </template>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar :class="$vuetify.breakpoint.lgAndUp ? 'px-12 nav-glass' : ''" flat color="transparent" absolute>
      <div style="width: 100%" class="d-flex align-center d-flex justify-space-between pt-4">
        <div class="d-flex logo__wrapper justify-space-between align-center">
          <v-toolbar-title>
            <nuxt-link to="/">
              <img src="/images/rendezvous-purple.png" class="logo mx-auto">
            </nuxt-link>
          </v-toolbar-title>

          <v-app-bar-nav-icon v-if="this.$vuetify.breakpoint.mdAndDown" @click.stop="sideNav.model = !sideNav.model"
            class="primary--text"></v-app-bar-nav-icon>
        </div>
        <!-- Nav for web -->
        <div class="d-flex align-center" v-if="$vuetify.breakpoint.lgAndUp">
          <v-btn nuxt to="#" class="font__15    primary--text  font-weight-bold" text>Discover</v-btn>
          <v-btn nuxt to="#events" class="font__15  primary--text  font-weight-bold" text>About us</v-btn>
          <v-btn nuxt to="#faq" class="font__15  primary--text  font-weight-bold" text>FAQs</v-btn>
          <v-btn nuxt to="#contact" class="font__15   primary--text  font-weight-bold" text>Contact us</v-btn>
        </div>
        <div class="d-flex align-center" v-if="$vuetify.breakpoint.lgAndUp">
          <v-btn nuxt to="#log-in" depressed class="mr-4 font__15 font-weight-bold" color="#432361" width="150"
            height="50" text>Log In</v-btn>
          <v-btn nuxt to="#sign-up" depressed class="mr-4 font__15 white--text font-weight-bold" color="#783EAD"
            width="180" height="50">Sign up</v-btn>
        </div>
      </div>
    </v-app-bar>
  </main>
</template>

<style lang="scss" scoped>
.v-btn {
  transition: 0.7s;
  color: white;

  @media (min-width: 1380px) {
    // font-size: 1rem !important;
  }


}

.logo__wrapper {
  @media (max-width: 1264px) {
    width: 100%;
  }
}

a {
  text-decoration: none;
}

.logo {
  width: 200px;

  @media (max-width: 600px) {
    width: 100px;
  }
}

.nav-glass {
  height: 78px !important;
  background: rgb(255 255 255 / 72%) !important;
  margin: 20px;
  border-radius: 20px !important;
  margin-top: 21px !important;
}
</style>

<script>
export default {
  data: () => ({
    sideNav: {
      model: false,
      type: 'persistent',
      clipped: false,
      floating: false,
      mini: false,
      stateless: true,
      scrolled: false
    },
    items: [{
      icon: 'mdi-home',
      text: 'HOME',
      to: '/'
    },
    {
      icon: 'mdi-find-replace',
      text: 'DISCOVER',
      to: '#discover'
    },
    {
      icon: 'mdi-information',
      text: 'ABOUT US',
      to: '#about'
    },
    {
      icon: 'mdi-head-question',
      text: 'FAQs',
      to: '#faq'
    },
    {
      icon: 'mdi-phone-message',
      text: 'CONTACT US',
      to: '#contact'
    },
    {
      icon: 'mdi-login',
      text: 'LOG IN',
      to: '#log-in'
    },
    {
      icon: 'mdi-account-plus',
      text: 'SIGN UP',
      to: '#sign-up'
    }
    ],
  })
}
</script>
