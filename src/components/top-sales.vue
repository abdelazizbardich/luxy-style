<template>
  <div class="top_sales">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <heroHeader
            title="TOP VENTE"
            subtitle="TOP VENTE DANS CETTE SEMAINE"
          />
          <div class="top_sales_grid">
            <productCard v-for="(i, index) in 16" :key="index" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.top_sales {
  .top_sales_grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
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
