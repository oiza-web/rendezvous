<template>
  <v-container fluid>
    <v-row>
      <v-col
        cols="12"
        lg="4"
        md="6"
        sm="12"
        v-for="(event, i) in allEvents"
        :key="i"
      >
        <v-card height="488" class="w-100" outlined :to="`/events/${event.id}`">
          <v-img :src="event.imageUrl" height="240" cover />
          <v-card-text class="primary--text font__12 font-weight-bold">{{
            event.title
          }}</v-card-text>
          <div class="">
            <div class="font__15 mx-4 font-weight-black primary--text">
              {{ formatDate(event.date) }}
            </div>
            <div class="font__14 mx-4 primary--text font-weight-light h-60">
              {{
                event.description.length > 220
                  ? event.description.substring(0, 220) + '...'
                  : event.description
              }}
            </div>
          </div>
          <div
            class="d-flex font__10 mx-4 my-6 primary--text font-weight-medium"
          >
            <div class="font-weight-bold font__15">View details</div>
            <div class="mt-1 ml-2">
              <svg
                width="16"
                height="17"
                viewBox="0 0 16 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <rect
                  width="16"
                  height="16"
                  transform="translate(0 0.5)"
                  fill="white"
                  style="mix-blend-mode: multiply"
                />
                <path
                  d="M5 3.5V4.5H11.295L3 12.795L3.705 13.5L12 5.205V11.5H13V3.5H5Z"
                  fill="#432361"
                />
              </svg>
            </div>
          </div>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  props: {
    allEvents: [],
  },
  data() {
    return {}
  },
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      const options = {
        weekday: 'long',
        month: 'long',
        day: 'numeric',
        year: 'numeric',
      }
      return date.toLocaleDateString('en-US', options)
    },
  },
}
</script>

<style lang="scss" scoped></style>
