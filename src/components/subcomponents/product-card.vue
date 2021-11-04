<template>
  <div class="product_card">
    <div class="header">
      <span class="price">999.99dh</span>
      <span class="stars">
        <i class="bi bi-star-fill"></i>
        <i class="bi bi-star-fill"></i>
        <i class="bi bi-star-fill"></i>
        <i class="bi bi-star-fill"></i>
        <i class="bi bi-star-fill"></i>
      </span>
    </div>
    <div class="thumbnail">
      <img src="@/assets/product.png" alt="" />
    </div>
    <div class="title">
      <span>Flared Shift Dress</span>
    </div>
    <div class="actions">
      <span class="add-to-cart">
        <i class="bi bi-cart-plus-fill"></i>Ajouter au panier
      </span>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.product_card {
  padding-block: 16px;
  padding-inline: 8px;
  max-width: 100%;
  .header {
    padding: 6px 12px;
    width: 100%;
    background-color: #51ffe4;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .price {
      text-transform: uppercase;
      font-weight: bold;
    }
    .stars {
      i {
        font-size: 12px;
        margin-inline: 2px;
        color: #04ac92;
      }
    }
  }
  .thumbnail {
    img {
      width: 100%;
      height: auto;
      border: 1px solid #51ffe4;
    }
  }
  .title {
    font-weight: bold;
    text-transform: uppercase;
    font-size: 24px;
    text-align: center;
    margin-block: 16px;
  }
  .actions {
    padding: 8px 16px;
    width: 100%;
    font-size: 20px;
    color: #ffffff;
    text-transform: uppercase;
    text-align: center;
    background-color: #04ac92;
    display: flex;
    justify-content: center;
    align-items: center;
    i {
      margin-inline-end: 8px;
      font-size: 24px;
    }
  }
}
</style>
<script>
export default {};
</script>
