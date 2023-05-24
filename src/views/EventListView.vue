<script setup>
import EventCard from '@/components/EventCard.vue'
import { ref } from 'vue'
const events = ref([
  {
    id: 5928101,
    category: 'animal welfare',
    title: 'Cat Adoption Day',
    description: 'Find your new feline  friend at this event.',
    location: 'Meow Town',
    date: 'January 28,2022',
    time: '12:00',
    petsallowed: true,
    organizer: 'Kat Laydee',
  },
  {
    id: 4582797,
    category: 'food',
    title: 'Community gardeneing',
    description: 'join us we tend to the community edible plants.',
    location: 'Flora city',
    date: 'March 14,2022',
    time: '10:00',
    petsallowed: true,
    organizer: 'fern pollins',
  },
  {
    id: 8419998,
    category: 'sustainability',
    title: 'Beach Cleanup',
    description: 'Help pick up trash along the shore.',
    location: 'Playa Del Carmen',
    date: 'January 22,2022',
    time: '11:00',
    petsallowed: false,
    organizer: 'carey Wales',
  },
])
</script>

<template>
  <h1>Events for Good</h1>
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
