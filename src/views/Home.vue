<template>
  <div class="max-w-md mx-auto px-8 py-8">
    <h2 class="text-7xl text-gray-900">Events</h2>
    <p class="mt-2 text-gray-600">A selection of great events.</p>
    <div class="mt-6 grid gap-y-6">
      <!-- lg:grid-cols-2 xl:grid-cols-3 -->
      <EventCard v-for="event in events" :key="event.id" :event="event" />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from '@/components/EventCard.vue'

export default {
  name: 'Home',
  components: {
    EventCard
  },
  data() {
    return {
      events: [
        {
          id: 5928101,
          category: 'animal welfare',
          title: 'Cat Adoption Day',
          description: 'Find your new feline friend at this event.',
          location: 'Meow Town',
          date: 'January 28, 2022',
          time: '12:00',
          petsAllowed: true,
          organizer: 'Kat Laydee',
          image: 'cat.jpg'
        },
        {
          id: 4582797,
          category: 'food',
          title: 'Community Gardening',
          description: 'Join us as we tend to the community edible plants.',
          location: 'Flora City',
          date: 'March 14, 2022',
          time: '10:00',
          petsAllowed: true,
          organizer: 'Fern Pollin',
          image: 'food.jpg'
        },
        {
          id: 8419988,
          category: 'sustainability',
          title: 'Beach Cleanup',
          description: 'Help pick up trash along the shore.',
          location: 'Playa Del Carmen',
          date: 'July 22, 2022',
          time: '11:00',
          petsAllowed: false,
          organizer: 'Carey Wales',
          image: 'beach.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="postcss" scoped>
h1 {
  @apply text-7xl text-blue-600;
}

.events {
  @apply md:container mx-auto;
}
</style>
