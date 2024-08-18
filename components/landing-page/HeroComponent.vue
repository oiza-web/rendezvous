<template>
  <section>
    <div class="hero-background-image"></div>
    <div class="hero-content d-flex justify-space-between">
      <div class="hero-content__text">
        Ready to Rock? Discover the Hottest <br />
        Events Here – Your Calendar's New Best <br />
        Friend!
      </div>
      <div class="hero-content__search d-flex justify-space-between align-center px-4">
        <div class="hero-content__search-box">Search for event</div>
        <!-- <v-divider vertical></v-divider> -->
        <div class="hero-content__search-box"></div>
        <div class="hero-content__search-categories">
          <v-select width="30" label="Categories" class="" color="black" dark item-color="white" focused="true"
            :items="['California', 'Colorado', 'Florida', 'Georgia', 'Texas', 'Wyoming']" variant="outlined"></v-select>
        </div>
        <v-btn color="#432361" class="font-weight-bold" depressed>Search</v-btn>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>

<style lang="scss">
.v-input.theme--dark.v-text-field.v-text-field--is-booted.v-select {
    width: 200px !important;
}
</style>
