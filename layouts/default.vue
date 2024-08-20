<template>
  <v-app id="default-layout">
    <Header />

    <v-main class="white ">
      <nuxt />
    </v-main>

    <Footer />
  </v-app>
</template>

<style lang="scss" scoped>
// @import url('https://fonts.googleapis.com/css?family=Allura&display=swap');
@import url('https://fonts.cdnfonts.com/css/gilroy-bold');

.main__footer {
  margin-top: 100px;

  @media (max-width: 1240px) {
    margin-top: unset;
  }
}
</style>
