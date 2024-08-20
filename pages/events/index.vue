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
    getAllEvents(){
      this.$axios.$get('/events').then((events) => {
        console.log(events.data.allEvents);
        this.events = events.data.allEvents
      })
    }
  },
  mounted() {
    this.getAllEvents();
  },
}
</script>

<style lang="scss" scoped></style>
