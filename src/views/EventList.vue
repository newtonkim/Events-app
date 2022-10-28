<template>
  <div class="events">
    <h1 class="head"> Venom Events</h1>
    <event-card v-for="event in events" :key="event.id" :event="event"/>
  </div>
</template>

<script>
import EventCard from "../components/EventCard.vue";

export default {
  name: "EventList",
  components: {
    EventCard,
  },

    data() {
    return {
      events: [
        {
        id: 4554443,
        category: "animal welfaire",
        title: "Dog adoption Day",
        description: "Find your new pet",
        location: "kings way",
        date: "October 28, 2022",
        time: "12:00",
        pestAllowed: true,
        organizer: "Newton",
        },

        {
        id: 4554467,
        category: "Food",
        title: "Matooke Show case Uganda",
        description: "Indeginous food",
        location: "Masaka",
        date: "April 12, 2022",
        time: "10:00",
        pestAllowed: true,
        organizer: "Juuko",
        },
        {
        id: 4554889,
        category: "Cars",
        title: "Subaru Forester Sti",
        description: "Modern subaru with AWD",
        location: "Namugongo",
        date: "Dec 05, 2022",
        time: "8:00",
        pestAllowed: true,
        organizer: "Nyamu",
        },
        {
        id: 4556432,
        category: "Art",
        title: "The Dodger",
        description: "The beam of life",
        location: "Hens Town",
        date: "January 17, 2022",
        time: "11:00",
        pestAllowed: true,
        organizer: "Mat",
        },
      
      ] 
    }
  },
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
