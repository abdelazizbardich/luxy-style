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
      <router-link to="/produit/1">
        <img src="@/assets/product.png" alt="" />
      </router-link>
      <router-link to="/categorie">
        <div class="category">T-SHIRTS</div>
      </router-link>
    </div>
    <div class="title">
      <router-link to="/produit/1">
        <span>Flared Shift Dress</span>
      </router-link>
    </div>
    <div class="actions">
      <router-link to="#"
        ><span class="add-to-cart">
          <i class="bi bi-cart-plus-fill"></i>Acheter maintenant
        </span></router-link
      >
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
    cursor: pointer;
    position: relative;
    img {
      width: 100%;
      height: auto;
      border: 1px solid #51ffe4;
    }
    .category {
      position: absolute;
      inset-inline-end: 15px;
      inset-block-end: 15px;
      color: #04ac92;
      font-size: 12px;
      &:hover {
        opacity: 0.5;
      }
    }
  }
  .title {
    font-weight: bold;
    text-transform: uppercase;
    font-size: 24px;
    text-align: center;
    margin-block: 16px;
    cursor: pointer;
    a {
      color: initial;
    }
  }
  .actions {
    padding: 8px 16px;
    width: 100%;
    font-size: 20px;
    color: #000000;
    text-transform: uppercase;
    text-align: center;
    background-color: #ffe600;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    a {
      color: unset;
    }
    &:hover {
      background-color: #ffe600;
      color: #000000;
      box-shadow: #ceb902 4px 7px 0px;
    }
    i {
      margin-inline-end: 8px;
      font-size: 24px;
    }
  }
}
@media screen and (max-width: 768px) {
  .product_card {
    .header {
      flex-direction: column;
      .stars {
        display: none;
      }
    }
    .thumbnail {
      .category {
        inset-block-end: 5px;
        inset-inline-end: 5px;
      }
    }
    .title {
      font-size: 12px;
      margin-block-end: 4px;
    }
    .actions {
      font-size: 10px;
      i {
        font-size: 10px;
      }
    }
  }
}
</style>
<script>
export default {
  methods: {
    addToCart() {
      alert("added to cart");
    },
  },
};
</script>
