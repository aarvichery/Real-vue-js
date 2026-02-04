<script setup>
import EventCard from '@/components/EventCard.vue'
import { ref } from 'vue'
import axios from 'axios'

const events = ref(null)

onMounted(() => {
  // get events from mock db when component is created
})
</script>

<template>
  <h1>Events For Good</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
