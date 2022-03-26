<template>
    <h1 class="flex justify-center mt-8 text-5xl uppercase md:text-6xl lg:text-7xl text-orange-600 ">
        {{props.pageHeading}}</h1>
</template>

<script setup>
import { defineProps } from "vue";
const props = defineProps({
  pageHeading: {
    type: String
  }
});
</script>