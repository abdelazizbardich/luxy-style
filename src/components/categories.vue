<template>
  <div class="categories">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <span class="hero_title">Nos Categories</span>
          <div class="categories_grid">
            <div class="category_item">
              <router-link to="#">
                <img src="@/assets/logo.png" alt="category image" />
              </router-link>
              <span class="category_title">Nos Categories</span>
            </div>
            <div class="category_item">
              <router-link to="#">
                <img src="@/assets/logo.png" alt="category image" />
              </router-link>
              <span class="category_title">Nos Categories</span>
            </div>
            <div class="category_item">
              <router-link to="#">
                <img src="@/assets/logo.png" alt="category image" />
              </router-link>
              <span class="category_title">Nos Categories</span>
            </div>
            <div class="category_item">
              <router-link to="#">
                <img src="@/assets/logo.png" alt="category image" />
              </router-link>
              <span class="category_title">Nos Categories</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.categories {
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
  .hero_title {
    font-size: 32px;
    font-weight: bold;
    text-transform: uppercase;
    text-shadow: #51ffe4 4px 7px 0px;
    margin-inline: auto;
    margin-block: 64px;
    display: block;
    width: fit-content;
  }
  .categories_grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    .category_item {
      text-align: center;
      padding: 8px;
      img {
        border: 1px solid #04ac92;
        background-color: #ffffff;
        border-radius: 16px;
        padding: 8px;
        display: block;
        margin-inline: auto;
        margin-block-end: 32px;
      }
      .category_title {
        display: block;
        text-align: center;
        margin-block-end: 63px;
        text-transform: uppercase;
        font-weight: bold;
        position: relative;
        margin-top: 25px;
        &::after {
          content: "";
          background-image: url("~@/assets/cat-shadow.svg");
          left: 0px;
          top: -50px;
          width: 100%;
          height: 50px;
          background-position: center center;
          background-size: 15px contain;
          background-repeat: no-repeat;
          position: absolute;
        }
      }
    }
  }
}
@media screen and (max-width: 768px) {
  .categories {
    .categories_grid {
      grid-template-columns: repeat(1, 1fr);
    }
  }
}
</style>
<script>
export default {};
</script>
