<template>
  <p class="flex flex-col justify-center w-3/4 box-content max-w-screen-md m-auto ">
    {{ props.cardInfo }}
  </p>
</template>

<script setup>
import { defineProps } from "vue";
const props = defineProps({
  cardInfo: {
    type: String,
    default: 'detail'
  }
});
</script>