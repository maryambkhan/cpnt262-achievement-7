<template>
<main class="bg-blue-400">
  <TheHeader />
  <PageHeading :pageHeading="'New Available'" />
   <div class="md:grid md:grid-cols-2">
    <!--first card-->
  <div class=" w-1/3   bg-white m-auto  mt-2">
  <CardImage :img="cardImage" />
  <CardHeader :cardTitle="cardTitle" />
  <CardInfo :cardInfo="cardInfo" />
  <CardPrice :cardPrice="cardPrice" />
   <button  class="text-justify round bg-yellow-600 mt-6">Add To Cart</button>
  </div>
  <!--second card-->
  <div class=" w-1/3  bg-white m-auto mt-2">
  <CardImage :img="cardsImage" />
  <CardHeader :cardTitle="cardsTitle" />
  <CardInfo :cardInfo="cardsInfo" />
  <CardPrice :cardPrice="cardsPrice" />
   <button  class="text-justify round bg-green-600 mt-6">Add To Cart</button>
  </div>
  <!-- Third card -->
  <div class=" w-1/3  bg-white m-auto mt-2">
  <CardImage :img="cardsImages" />
  <CardHeader :cardTitle="cardsHeader" />
  <CardInfo :cardInfo="cardsDetail" />
  <CardPrice :cardPrice="cardsPrices" />
  <button  class="text-justify round bg-red-600 mt-6">Add To Cart</button>
  </div>
  </div>
   <TheFooter :title="'&copy; Maryam khan 2022'" />
  </main>
 
</template>

// imports
<script setup>
import TheHeader from "./components/layout/TheHeader.vue";
import TheFooter from "./components/layout/TheFooter.vue";
import PageHeading from "./components/ui/PageHeading.vue";
import CardHeader from "./components/cards/CardHeader.vue";
import CardImage from "./components/cards/CardImage.vue";
import CardInfo from "./components/cards/CardInfo.vue";
import CardPrice from "./components/cards/cardPrice.vue";



// first card
const cardTitle = "Lipstic";

const cardInfo = "Lorem Ipsum is simply dummy text ";
const cardPrice = "$60";

const cardImage = {
  url : "https://images.pexels.com/photos/2639947/pexels-photo-2639947.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2",
  alt:"product"
}

// second card
const cardsTitle = "Brushes";

const cardsInfo = "Lorem Ipsum is simply dummy text ";
const cardsPrice = "$20";

const cardsImage = {
  url : "https://images.pexels.com/photos/6527699/pexels-photo-6527699.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2",
  alt:"product"
}

// third card
const cardsHeader = "EyeLiner";

const cardsDetail = "Lorem Ipsum is simply dummy text";
const cardsPrices = "$40";

const cardsImages = {
  url : "https://images.pexels.com/photos/2697787/pexels-photo-2697787.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
  alt:"product"
}
</script>


