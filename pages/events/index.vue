<template>
  <div class="other-page mx-6">
    <Events :all-events="events" />
  </div>
</template>

<script lang="js">
import Events from "/components/Events";
export default {
  data() {
    return {
      events: []
    }
  },
  methods:{
    async getAllEvents() {
      try {
        const response = await this.$axios.$get('/events');
        console.log(response.data.allEvents);
        this.events = response.data.allEvents;
      } catch (error) {
        console.error('Error fetching events:', error);
      }
    },
  },
  mounted() {
    this.getAllEvents();
  },
}
</script>

<style lang="scss" scoped></style>
