<template>
  <RouterLink class="event-link" :to="{ name: 'EventDetails', params: {id: event.id } }">
    <div class="event-card">
      <span> @ {{ event.time }} on {{ event.date }}</span>
      <h4>{{ event.title }}</h4>
    </div>
  </RouterLink>
</template>

<script>
export default {
  name: "EventCard",
  props: {
    event: Object,
  },
};
</script>

<style scoped>
.event-card {
  padding: 20px;
  font-size: 20px;
  width: 350px;
  cursor: pointer;
  border: 1px solid #d7d109;
  margin-bottom: 18px;
}
.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}

.event-link {
   color: #fff; 
   text-decoration: none;
}
</style>
