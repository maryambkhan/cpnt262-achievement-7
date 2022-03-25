<template>
<div class="flex justify-center">
  <img
    :src="props.img.url"
    :alt="props.img.alt"
    class=" mt-6 ml-2 w-2/4 h-2/4"
  />
</div>
</template>


<script setup>
import { defineProps } from "vue";
const props = defineProps({
  img: {
    type: Object,
  }
});
</script>
