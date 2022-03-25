<template>
  <main class="bg-blue-400">
    <TheHeader />
    <PageHeading :pageHeading="'New Available'" />
    <card-layout v-for="cards in cards" :key="cards.id">
      <card-layout-image :url="cards.image" />
      <card-layout-title>{{ cards.title }}</card-layout-title>
      <card-layout-info>{{ cards.info }}</card-layout-info>
      <card-layout-price>{{ cards.price }}</card-layout-price>
      <card-layout-action
        class="
          bg-emerald-300
          text-slate-900
          hover:bg-emerald-400 hover:shadow-md
          shadow-emerald-600
        "
        >Add to Cart</card-layout-action
      >
    </card-layout>

    <TheFooter :title="'&copy; Maryam khan 2022'" />
  </main>
</template>

// imports
<script setup>
import TheHeader from "./components/layout/TheHeader.vue";
import TheFooter from "./components/layout/TheFooter.vue";
import PageHeading from "./components/ui/PageHeading.vue";
import CardLayout  from "./components/cards/CardLayout.vue";
import CardHeader from "./components/cards/CardHeader.vue";
import CardImage from "./components/cards/CardImage.vue";
import CardInfo from "./components/cards/CardInfo.vue";
import CardPrice from "./components/cards/cardPrice.vue";



// first card
const cards = [
{
    title :  "Lipstic",
    info : "Lorem Ipsum is simply dummy text ",
    price : "$60",
   
   
},

// second card

   { 
     title: "Brushes",
    info: "Lorem Ipsum is simply dummy text ",
    price: "$20",
    
},

// third card
{
  title : "EyeLiner",
  info : "Lorem Ipsum is simply dummy text",
  price : "$40",
  
}];
</script>


