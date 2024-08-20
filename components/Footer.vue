<template>
  <main class="bg">
    <v-container fluid class="py-9 mx-4">
      <v-row class="justify-space-between ">
        <v-col cols="12" lg="4">
          <img src="/images/rendezvous-logo.png" height="40" />
          <div class="font-weight-light font__12 my-4">Your Personal Event Sherpa: Curating <br> Awesome, One Click at a
            Time.
          </div>

        </v-col>

        <v-col sm="12" lg="8" v-if="$vuetify.breakpoint.smAndUp">
          <div class="d-flex justify-space-between">

            <v-col cols="4" class="font-weight-thin font__12 ml-7" lg="3">
              <div class="font-weight-bold font__16">Features</div>
              <div class="mt-1">Event discovery</div>
              <div class="mt-1">Ticketing</div>
            </v-col>

            <v-col cols="4" class="font-weight-light font__12" lg="3">
              <div class="font-weight-bold font__16">Company</div>
              <div class="mt-1">About us</div>
              <div class="mt-1">FAQs</div>
              <div class="mt-1">Careers</div>
              <div class="mt-1">Support</div>

            </v-col>

            <v-col md="2" :class="['font-weight-medium font__12', { 'd-none': $vuetify.breakpoint.mdAndDown }]" lg="3">
              <div class="font-weight-bold font__16">Contact us</div>
              <div class="mt-1 font-weight-bold">info@events.com</div>
              <div class="mt-1">+234 701 345 6789</div>
              <div class="mt-1">Race Course, 8/9 Marina, Onikan, Lagos Lagos, 4aa Force Rd, Lagos Island 102273, Lagos
              </div>
            </v-col>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </main>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.bg {
  background: #432361;
  color: #FFFFFF;
}
</style>
