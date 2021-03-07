<template>
  <div class="event-card-tw">
    <img
      className="h-32 w-32 flex-shrink  object-cover object-center"
      v-bind:src="require(`../assets/${event.image}`)"
    />
    <router-link
      class="px-6 py-4"
      :to="{ name: 'EventDetails', params: { id: event.id } }"
    >
      <div class="px-6 py-4">
        <h3 class="text-lg font-semibold text-gray-800">{{ event.title }}</h3>
        <p class="text-gray-600">@{{ event.time }} on {{ event.date }}</p>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  props: {
    event: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>

.event-card-tw {
  @apply flex items-center rounded-lg text-center bg-white shadow-lg overflow-hidden hover:scale-100 hover:shadow-lg transform;
}
</style>
