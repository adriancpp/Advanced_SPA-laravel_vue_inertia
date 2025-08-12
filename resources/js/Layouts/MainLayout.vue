<template>
  <Link href="/">IndexPage</Link>&nbsp;
  <Link href="/hello">ShowPage</Link>&nbsp;
  <Link href="/listing">List</Link>&nbsp;
  <Link href="/listing/create">Create</Link>
  <!-- <div>The page with time {{ timer }}</div> -->
  <div v-if="flashSuccess" class="success">
    {{ flashSuccess }}
  </div>

  <slot>default</slot>
</template>

<script setup>
import {Link, usePage} from '@inertiajs/vue3'
import { computed } from 'vue'

// page.props.value.flash.success
const page = usePage()
const flashSuccess = computed(
  () => page.props.flash.success,
)

// import {ref} from 'vue'

// const timer = ref(0)
// setInterval(() => timer.value++, 1000)
</script>

<style scoped>
  .success {
    background-color: green;
    color: white;
  }
</style>