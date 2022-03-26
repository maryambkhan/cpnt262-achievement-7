<template>
<div class="mt-4">
<footer class="grid place-items-center text-center h-32 text-orange-900">
  <p>{{ props.title }}</p>
</footer>
</div>
</template>

<script setup>
import {defineProps} from 'vue';
const props = defineProps({
  title: {
    type: String,
    default: '&copy; 2022'
  }
});
</script>