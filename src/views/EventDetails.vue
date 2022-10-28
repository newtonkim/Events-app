<template>

  <div class="event-card" v-if="event">
    <h1>{{ event.title }}</h1>
    <p>{{ event.time }} on {{ event.date }} @ {{ event.location }}</p>
    <p>{{ event.description }}</p>
  </div>
</template>

<script>
import EventService from "../Services/EventService.js";

export default {
  props: {
    id: {
      type: String,
      required: true
    }
  },

  data() {
    return {
        event: null,
       
    }
  },
  created() {
    EventService.getEvent(this.id)
      .then((response) => {
        this.event = response.data;
      })

      .catch((error) => {
        console.log(error);
      })
  },
};
</script>

<style>
.event-card {
  padding: 10px;
  font-size: 25px;
  width: 480px;
  border: 1px solid #d7d109;
  margin-bottom: 18px;
}
</style>