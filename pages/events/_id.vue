<template>
  <section class="mx-6">
    <Details class="other-page"  :event-details="eventDetails" />
  </section>
</template>

<script lang="js">
import Details from "/components/Details";
export default {
  name: 'EventDetailsPage',
data(){
 return{
   eventDetails: {}
 }
},
methods: {
  getOneEvent(){
    const id = this.$route.params.id
    this.$axios.$get(`/events/${id}`).then((events) => {
      console.log(events.data.event);
      this.eventDetails = events.data.event
    })
  }
},
mounted(){
  this.getOneEvent()
}
}
</script>

<style lang="scss"></style>
