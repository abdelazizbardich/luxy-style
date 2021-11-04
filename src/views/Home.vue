<template>
  <div class="home">
    <Header />
    <HeroSlider />
    <Categories />
    <Cards />
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/header.vue";
import HeroSlider from "@/components/hero-slider.vue";
import Categories from "@/components/categories.vue";
import Cards from "@/components/cards.vue";
export default {
  name: "Home",
  components: {
    Header,
    HeroSlider,
    Categories,
    Cards,
  },
};
</script>
