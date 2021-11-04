<template>
  <div class="instargm_feed">
    <div class="container">
      <div class="row">
        <div class="col-md-10 offset-md-1">
          <heroHeader title="@ SUIVEZ-NOUS SUR" subtitle="INSTAGRAM" />
          <div class="instagram_grid">
            <Post v-for="(i, index) in 9" :key="index" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.instargm_feed {
  margin-block-end: 64px;
  .instagram_grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }
}
</style>
<script>
import heroHeader from "@/components/subcomponents/hero-title.vue";
import Post from "@/components/subcomponents/instagram-post.vue";
export default {
  components: {
    heroHeader,
    Post,
  },
};
</script>
