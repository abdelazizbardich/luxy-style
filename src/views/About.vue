<template>
  <div class="about">
    <Header />
    <PageTitle :title="'à proppos'" />
    <div class="container">
      <div class="row py-5">
        <div class="col-md-6">
          <img src="@/assets/luxystyle-logo.svg" class="w-100 mb-3" alt="" />
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sit
            amet mauris vel dui pulvinar vulputate at non libero. Maecenas
            placerat ipsum sit amet dui volutpat pellentesque. Etiam euismod
            tincidunt ante, sed interdum orci tempor nec. Fusce euismod, odio et
            pellentesque tempus, libero velit facilisis libero, eu porta felis
            nulla nec metus. Praesent viverra eget dui vitae scelerisque.
            Suspendisse placerat vestibulum purus,
          </p>
          <p>
            tincidunt cursus massa ullamcorper nec. Praesent a tortor sed orci
            egestas pretium. Sed aliquam non ipsum sit amet tristique.
            Pellentesque luctus consectetur metus. Duis risus diam, iaculis quis
            elit vitae, sagittis lobortis nibh. In hac habitasse platea
            dictumst. Phasellus ut nisi ac ipsum tempus ullamcorper. Nam non
            accumsan lectus. Praesent fringilla, odio sed ullamcorper auctor,
            orci tellus iaculis sapien, quis efficitur odio eros in leo. In
            vitae interdum augue. Vivamus malesuada, nisl eu malesuada tempor,
            est quam facilisis risus, at congue tortor elit tempor sem.
          </p>
          <p>
            Proin lorem lacus, fringilla ut sapien vel, ornare cursus enim.
            Maecenas nibh risus, aliquet ac gravida fermentum, mattis vel est.
            Integer accumsan, urna et imperdiet vulputate, diam neque ultrices
            lacus, ac scelerisque nulla mauris in ipsum. Mauris in auctor neque,
            vel feugiat ipsum. Class aptent taciti sociosqu ad litora torquent
            per conubia nostra, per inceptos himenaeos.
          </p>
          <p>
            Aliquam aliquam hendrerit nulla quis tempor. Aliquam pharetra, orci
            ut malesuada facilisis, quam mi pulvinar nisi, non vehicula leo
            velit eget ex. Suspendisse sit amet maximus erat. Etiam posuere,
            magna nec fringilla ultrices, purus eros eleifend purus, eget
            venenatis arcu ligula at diam. Vestibulum ultrices nulla fermentum
            lacinia consequat.
          </p>
        </div>
        <div class="col-md-6">
          <img src="@/assets/about.png" alt="about us" />
        </div>
      </div>
    </div>
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
