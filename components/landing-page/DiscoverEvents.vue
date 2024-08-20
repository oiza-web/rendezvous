<template>
  <section>
    <v-container fluid class="my-14">
      <v-row class="mx-auto">
        <v-col cols="12" lg="4" md="4" sm="12">
          <div class="mx-auto">
            <h4 class="font__32">Discover a World of Events <br> Tailored Just for You.</h4>
            <v-btn color="#783EAD" class="mt-6 font__16 font-weight-bold white--text" depressed to="/events" >View all events</v-btn>
          </div>
        </v-col>
        <v-col cols="12" lg="4" md="4" sm="12">
          <v-card flat>
            <v-img class="align-center" height="240" lazy-src="/images/online-events.png" cover>
              <p class="accent--text text-center font__24 font-weight-medium ">Online Events</p>
            </v-img>
          </v-card>
          <v-card class="my-6" flat>
            <v-img class="align-center text-white" height="240"
              lazy-src="/images/hybrid-events.png" cover>
              <p class="accent--text text-center font__24 font-weight-medium">Hybrid Events</p>
            </v-img>
          </v-card>
        </v-col>
        <v-col cols="12" lg="4" md="4" sm="12">
          <v-card  flat>
            <v-img class="align-center text-white" height="240" lazy-src="/images/physical-events.png" cover>
              <p class="accent--text text-center font__24 mx-auto font-weight-medium">Physical Events</p>
            </v-img>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {

    }
  }
}
</script>

<style lang="scss">
.v-image__image.v-image__image--preload.v-image__image--cover {
  filter: brightness(50%) !important;
}
</style>
