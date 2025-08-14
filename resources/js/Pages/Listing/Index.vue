<template>
  <div v-for="listing in listings" :key="listing.id">
    <div>
      <Link :href="`/listing/${listing.id}`">
        <ListingAddress :listing="listing" />
      </Link>
    </div>
    <div>
      <Link :href="`/listing/${listing.id}/edit`" as="button">Edit</Link>
    </div>
    <div>
      <Link :href="`/listing/${listing.id}`" method="delete" as="button">Delete</Link>
    </div>
  </div>
</template>

<script setup>
import ListingAddress from '@/Components/ListingAddress.vue'
import { Link } from '@inertiajs/vue3'
defineProps({
  listings: Array,
})
</script>