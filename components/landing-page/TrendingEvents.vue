<template>
  <section class="mt-8">
    <v-container fluid>
      <div class="d-flex justify-space-between px-12 my-4 ">
        <h4 class="font__32">Trending events</h4>
        <div class="d-flex font__10 primary--text font-weight-medium">
          <div class="font-weight-bold font__15 ">View all Trending events</div>
          <div class="mt-1 ml-2">
            <svg width="16" height="17" viewBox="0 0 16 17" fill="none" xmlns="http://www.w3.org/2000/svg">
              <rect width="16" height="16" transform="translate(0 0.5)" fill="white" style="mix-blend-mode: multiply" />
              <path d="M5 3.5V4.5H11.295L3 12.795L3.705 13.5L12 5.205V11.5H13V3.5H5Z" fill="#432361" />
            </svg>
          </div>
        </div>
      </div>
      <v-row>
        <v-col cols="12" lg="4" md="6" sm="12" v-for="(event, i) in events" :key="i">
          <v-card height="488" flat outlined to="/event-details">
            <v-img :src="event.image" height="280"  />
            <v-card-text class="primary--text font__12 font-weight-bold">{{
              event.title
              }}</v-card-text>
            <div class="">
              <div class="font__15 mx-4 font-weight-black primary--text">
                {{ event.date }}
              </div>
              <div class="font__14 mx-4 primary--text font-weight-light ">
                {{ event.description }}
              </div>
            </div>
            <div class="d-flex font__10 mx-4 my-6 primary--text font-weight-medium">
              <div class="font-weight-bold font__15 ">View details</div>
              <div class="mt-1 ml-2">
                <svg width="16" height="17" viewBox="0 0 16 17" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <rect width="16" height="16" transform="translate(0 0.5)" fill="white"
                    style="mix-blend-mode: multiply" />
                  <path d="M5 3.5V4.5H11.295L3 12.795L3.705 13.5L12 5.205V11.5H13V3.5H5Z" fill="#432361" />
                </svg>
              </div>
            </div>
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
      events: [
        {
          title: 'ISWIS Live show',
          image: '/images/two-ladies.png',
          date: `Sun, Oct 3rd 6pm`,
          description:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
          numberTicketsLeft: '5',
          daysLeft: 2,
        },
        {
          title: 'ISWIS Live show',
          image: '/images/nativ.png',
          date: `Sun, Oct 3rd 6pm`,
          description:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
          numberTicketsLeft: '5',
          daysLeft: 2,
        },
        {
          title: 'ISWIS Live show',
          image: '/images/basket-mouth.png',
          date: `Sun, Oct 3rd 6pm`,
          description:
            '$Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
          numberTicketsLeft: '5',
          daysLeft: 2,
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped></style>
