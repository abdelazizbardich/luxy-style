<template>
  <div class="new_arrivals">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <heroHeader
            title="Nouvelles Arrivées"
            subtitle="TOP VENTE DANS CETTE SEMAINE"
          />
          <div class="new_arrivals_grid">
            <productCard v-for="(i, index) in 16" :key="index" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.new_arrivals {
  .new_arrivals_grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
  }
}
@media screen and (max-width: 768px) {
  .new_arrivals {
    padding-block-end: 32px;
    .new_arrivals_grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
    }
  }
}
</style>
<script>
import heroHeader from "@/components/subcomponents/hero-title.vue";
import productCard from "@/components/subcomponents/product-card.vue";
export default {
  components: {
    heroHeader,
    productCard,
  },
};
</script>
