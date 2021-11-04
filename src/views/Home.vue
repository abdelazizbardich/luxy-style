<template>
  <div class="home">
    <Header />
    <HeroSlider />
    <Categories />
    <Cards />
    <NewArrival />
    <TopSales />
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/header.vue";
import HeroSlider from "@/components/hero-slider.vue";
import Categories from "@/components/categories.vue";
import Cards from "@/components/cards.vue";
import NewArrival from "@/components/new-arrival.vue";
import TopSales from "@/components/top-sales.vue";
export default {
  name: "Home",
  components: {
    Header,
    HeroSlider,
    Categories,
    Cards,
    NewArrival,
    TopSales,
  },
};
</script>
