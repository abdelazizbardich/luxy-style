<template>
  <div class="category_item">
    <router-link to="#">
      <img src="@/assets/category.png" alt="category image" />
    </router-link>
    <span class="category_title">
      <router-link to="#">Nos Categories</router-link>
    </span>
  </div>
</template>
<style lang="scss" scoped>
.category_item {
  text-align: center;
  padding: 8px;
  &:hover {
    img {
      transform: translateY(-15px);
    }
  }
  img {
    transition: 0.5s;
    border: 4px solid #c1faf1;
    background-color: #ffffff;
    border-radius: 16px;
    padding: 3px;
    display: block;
    margin-inline: auto;
    margin-block-end: 32px;
    width: 100%;
  }
  .category_title {
    display: block;
    text-align: center;
    margin-block-end: 63px;
    text-transform: uppercase;
    font-weight: bold;
    position: relative;
    margin-top: 25px;
    a {
      color: initial;
      display: block;
      transition: 0.3s;
      &:hover {
        transform: scale(1.1);
      }
    }
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
@media screen and (max-width: 768px) {
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
</style>
<script>
export default {};
</script>
