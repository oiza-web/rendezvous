<template>
  <section>
    <div class="hero-background-image"></div>
    <v-row>
      <v-col cols="12" lg="6" md="6" sm="12">
        <div class="hero-content__text font__32">
          Ready to Rock? Discover the Hottest <br />
          Events Here – Your Calendar's New Best <br />
          Friend!
        </div>
      </v-col>
      <v-col cols="12" lg="6" md="6" sm="12">
        <div class="hero-content__search d-flex justify-space-between align-center px-4">
          <div class="hero-content__search-box">Search for event</div>
          <v-divider vertical></v-divider>
          <div class="hero-content__search-box"></div>
          <div class="hero-content__search-categories">
            <v-select width="30" label="Categories" class="" color="black" dark item-color="white" focused="true"
              :items="['California', 'Colorado', 'Florida', 'Georgia', 'Texas', 'Wyoming']"
              variant="outlined"></v-select>
          </div>
          <v-btn color="#783EAD" class="font-weight-bold white--text" depressed>Search</v-btn>
        </div>
      </v-col>
    </v-row>
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
