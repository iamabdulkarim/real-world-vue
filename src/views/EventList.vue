<template>

  <div class="list">
    <h1>This is an event page</h1>
    <EventCard/>
    <BaseIcon/>
      
  
  </div>
</template>

<script>
import EventCard from '@/components/EventCard.vue';
import BaseIcon from '../components/BaseIcon.vue';
  export default {
    components: {
    EventCard,
    BaseIcon
},
  }
</script>

<style lang="scss" scoped>

</style>