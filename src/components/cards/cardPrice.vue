<template>
  <p class="flex flex-col justify-center box-content max-w-screen-md text-center m-auto ">
    {{ props.cardPrice }}
  </p>
</template>

<script setup>
import { defineProps } from "vue";
const props = defineProps({
  cardPrice: {
    type: String,
    default: 'price'
  }
});
</script>