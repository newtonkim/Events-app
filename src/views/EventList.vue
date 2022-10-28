<template>
  <div class="events">
    <h1 class="head"> Venom Events</h1>
    <event-card v-for="event in events" :key="event.id" :event="event"/>
  </div>
</template>

<script>
import EventCard from "../components/EventCard.vue";
import EventService from '../Services/EventService.js'

export default {
  name: "EventList",
  components: {
    EventCard,
  },

    data() {
    return {
      events: null
    }
  },
  created() {
    EventService.getEvents()
    .then(response => {

      this.events = response.data
      // console.log('events:', response.data);
    })
      .catch(error => {
        console.log(error);
    })
  }
}
</script>

<style scoped>
.events{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.head{

  padding-bottom:20px ;
}
</style>
