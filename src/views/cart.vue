<template>
  <div class="cart">
    <Header />
    <PageTitle :title="'Panier'" />

    <Footer />
  </div>
</template>
<style lang="scss" scoped>
@media screen and (max-width: 768px) {
}
</style>
<script>
import Header from "@/components/header.vue";
import Footer from "@/components/footer.vue";
import PageTitle from "@/components/page-title.vue";
export default {
  components: {
    Header,
    Footer,
    PageTitle,
  },
};
</script>
