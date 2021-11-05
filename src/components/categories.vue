<template>
  <div class="categories">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <heroHeader title="Nos Categories" />
          <div class="categories_grid">
            <CategoryCard v-for="(i, index) in 4" :key="index" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.categories {
  background-color: #f7f8fa;
  min-height: 400px;
  position: relative;
  perspective: 500px;
  overflow: hidden;
  &::after {
    content: "";
    position: absolute;
    background-color: #c1faf1;
    width: 100%;
    bottom: 0px;
    top: 60%;
    transform: rotateX(45deg);
    z-index: -1;
  }
  .categories_grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
  }
}
@media screen and (max-width: 768px) {
  .categories {
    padding-block-end: 32px;
    &::after {
      display: none;
    }
    .categories_grid {
      justify-items: center;
      grid-template-columns: repeat(2, 1fr);
      .category_item {
        .category_title {
          margin-block-start: 4px;
          margin-block-end: 8px;
          &::after {
            display: none;
          }
        }
        img {
          width: 100%;
          margin-bottom: 4px;
        }
      }
    }
  }
}
</style>
<script>
import heroHeader from "@/components/subcomponents/hero-title.vue";
import CategoryCard from "@/components/subcomponents/category-card.vue";
export default {
  components: {
    heroHeader,
    CategoryCard,
  },
};
</script>
