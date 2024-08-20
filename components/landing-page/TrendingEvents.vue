<template>
  <section class="mt-8">
    <v-container fluid>
      <div class="d-flex justify-space-between px-12 my-4 ">
        <h4 class="font__32">Trending events</h4>
        <nuxt-link to="/events">
          <div class="d-flex font__10 primary--text font-weight-medium">
            <div class="font-weight-bold font__15 ">View all Trending events</div>
            <div class="mt-1 ml-2">
              <svg width="16" height="17" viewBox="0 0 16 17" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect width="16" height="16" transform="translate(0 0.5)" fill="white"
                  style="mix-blend-mode: multiply" />
                <path d="M5 3.5V4.5H11.295L3 12.795L3.705 13.5L12 5.205V11.5H13V3.5H5Z" fill="#432361" />
              </svg>
            </div>
          </div>
        </nuxt-link>
      </div>
      <Events :all-events="events" />
    </v-container>
  </section>
</template>

<script lang="js">
import Events from '/components/Events'
export default {
  components: {
    Events
  },
  data() {
    return {
      events: [
        {
          title: 'ISWIS Live show',
          imageUrl: '/images/two-ladies.png',
          date: `Sun, Oct 3rd 6pm`,
          description:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
          numberTicketsLeft: '5',
          daysLeft: 2,
        },
        {
          title: 'ISWIS Live show',
          imageUrl: '/images/nativ.png',
          date: `Sun, Oct 3rd 6pm`,
          description:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
          numberTicketsLeft: '5',
          daysLeft: 2,
        },
        {
          title: 'ISWIS Live show',
          imageUrl: '/images/basket-mouth.png',
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
