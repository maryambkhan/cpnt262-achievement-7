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

// first card
const cards = [
  {
    title: "Lipstic",
    info: "Lorem Ipsum is simply dummy text ",
    price: "$60",
    image : require(`./assets/images/blush.jpeg`),
  },

  // second card

  {
    title: "Brushes",
    info: "Lorem Ipsum is simply dummy text ",
    price: "$20",
    size: "S",
    image : require(`./assets/images/combo.jpeg`),
  },

  // third card
  {
    title: "EyeLiner",
    info: "Lorem Ipsum is simply dummy text",
    price: "$40",
    size: "M,S",
    image : require(`./assets/images/liner.jpeg`),
  },
];
</script>

<style>
body{
  background-color:cadetblue;
}
</style>
