<template>
  <section>
    <HeroComponent />
    <TrendingEvents />
    <DiscoverEvents />
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
  }
}
</script>
