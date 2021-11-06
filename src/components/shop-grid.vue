<template>
  <div class="shop_grid">
    <div class="container-md">
      <div class="row">
        <div class="col-12">
          <div class="shop_grid_grid">
            <productCard v-for="(i, index) in 32" :key="index" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.shop_grid {
  margin-block-end: 64px;
  .shop_grid_grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
  }
}
@media screen and (max-width: 768px) {
  .shop_grid {
    margin-block-end: 32px;
    padding-block-end: 32px;
    .shop_grid_grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
    }
  }
}
</style>
<script>
import productCard from "@/components/subcomponents/product-card.vue";
export default {
  components: {
    productCard,
  },
};
</script>
