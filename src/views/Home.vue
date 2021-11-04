<template>
  <div class="home">
    <Header />
    <HeroSlider />
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/header.vue";
import HeroSlider from "@/components/hero-slider.vue";
export default {
  name: "Home",
  components: {
    Header,
    HeroSlider,
  },
};
</script>
