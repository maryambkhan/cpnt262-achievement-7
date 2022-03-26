<template>
  <main>
    <TheHeader />
    <PageHeading :pageHeading="'New Available'" />
    
    <div class="flex flex-wrap justify-center mt-8">
      <card-layout v-for="card in cards" :key="card.id">
        <card-image :url="card.image" />
        <card-header>{{ card.title }}</card-header>
        <card-info>{{ card.info }}</card-info>
        <card-price>{{ card.price }}</card-price>
        <card-size>{{ card.size }}</card-size>
        <card-tag v-if="card.tags">{{ card.tags }}</card-tag>
        <card-action>Add to Cart</card-action>
      </card-layout>
      
    </div>
    <TheFooter :title="'&copy; Maryam khan 2022'" />
  </main>
</template>

<script setup>
import TheHeader from "./components/layout/TheHeader.vue";
import TheFooter from "./components/layout/TheFooter.vue";
import PageHeading from "./components/ui/PageHeading.vue";
import CardLayout from "./components/cards/CardLayout.vue";
import CardHeader from "./components/cards/CardHeader.vue";
import CardImage from "./components/cards/CardImage.vue";
import CardInfo from "./components/cards/CardInfo.vue";
import CardPrice from "./components/cards/CardPrice.vue";
import CardSize from "./components/cards/CardSize.vue";
import CardAction from "./components/cards/CardAction.vue";
import CardTag from "./components/cards/CardTag.vue";


// first card
const cards = [
  {
    title: "Lipstic",
    info: "Lorem Ipsum is simply dummy text ",
    price: "$60",
    size: "S,M,L",
    image: require(`./assets/images/blush.jpeg`),
    tags: "Pink,Red,Brown",
  },

  // second card

  {
    title: "Brushes",
    info: "Lorem Ipsum is simply dummy text ",
    price: "$20",
    size: "S",
    image: require(`./assets/images/combo.jpeg`),
   tags: "Pink,Red,Brown",
  },

  // third card
  {
    title: "EyeLiner",
    info: "Lorem Ipsum iss simply dummy text",
    price: "$40",
    size: "M,S",
    image: require(`./assets/images/liner.jpeg`),

  },
];
</script>

<style>
body {
  background-color: cadetblue;
}
</style>
