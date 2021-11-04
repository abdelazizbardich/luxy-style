<template>
  <div class="latested_blogs">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <heroHeader
            title="DERNIÈRE DU BLOG"
            subtitle="LES NOUVELLES LES PLUS FRAÎCHES ET LES PLUS EXCITANTES"
          />
          <div class="latested_blogs_grid">
            <BlogCard v-for="(i, index) in 3" :key="index" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.latested_blogs {
  .latested_blogs_grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    margin-block-end: 32px;
  }
}
</style>
<script>
import BlogCard from "@/components/subcomponents/blog-card.vue";
import heroHeader from "@/components/subcomponents/hero-title.vue";
export default {
  components: {
    BlogCard,
    heroHeader,
  },
};
</script>
