<template>
  <section>
    <HeroComponent  />
    <TrendingEvents :events="events" class="mx-4" />
    <DiscoverEvents  class="mx-4"/>
  </section>
</template>

<script lang="js">
import HeroComponent from '/components/landing-page/HeroComponent'
import TrendingEvents from '/components/landing-page/TrendingEvents'
import DiscoverEvents from '/components/landing-page/DiscoverEvents'
export default {
  name: 'IndexPage',
  components:{
    HeroComponent,
    TrendingEvents,
    DiscoverEvents
  },
  data() {
    return {
      events: []
    }
  },
  methods: {
    async getAllEvents() {
      try {
        const response = await this.$axios.$get('/events');
        this.events = response.data.allEvents.slice(0, 3);;
      } catch (error) {
        throw error
v      }
    },
  },
  mounted() {
    this.getAllEvents();
  },
}
</script>
