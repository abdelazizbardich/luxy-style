<template>
  <div class="fixed_cart" :style="!show ? 'transform: translateX(150%);' : ''">
    <div class="container">
      <div class="row header">
        <div class="col"><span class="title">Panier</span></div>
        <div class="col-auto">
          <span class="close"><i class="bi bi-x-circle-fill"></i></span>
        </div>
        <div class="col-12"><hr /></div>
      </div>
      <div class="row body">
        <CartItem v-for="(i, index) in 7" :key="index" />
      </div>
      <div class="row total_price">
        <div class="col">Total</div>
        <div class="col-auto">999.99DH</div>
      </div>
      <div class="row footer">
        <div class="col-12"><hr /></div>
        <div class="col-12 view_cart">
          <router-link to="#">Voir le painer</router-link>
        </div>
        <div class="col-12 finish_order">
          <router-link to="#">Finaliser la commande</router-link>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.fixed_cart {
  background-color: #f7f8fa;
  width: 360px;
  max-width: 100%;
  height: calc(100vh - 60px);
  position: fixed;
  inset-inline-end: 0px;
  inset-block-end: 0px;
  inset-block-start: 60px;
  z-index: -1;
  box-shadow: #2ead9a62 -16px 0px 32px;
  display: flex;
  align-items: center;
  transition: 0.3s;
  .header {
    .title {
      font-size: 32px;
      text-transform: uppercase;
      font-weight: bold;
      color: #04ac92;
    }
    .close {
      color: #ff0033;
      font-size: 30px;
      cursor: pointer;
      transition: 0.3s;
      display: inline-block;
      &:hover {
        transform: scale(1.1);
      }
    }
    hr {
      border: none;
      height: 2px;
      background-color: #51ffe4;
    }
  }
  .body {
    height: 53vh;
    overflow-y: auto;
    padding-block: 16px;
  }
  .total_price {
    padding-block-start: 16px;
    font-weight: bold;
  }
  .footer {
    hr {
      border: none;
      height: 2px;
      background-color: #51ffe4;
    }
    .view_cart {
      a {
        background-color: #04ac92;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #ffffff;
        padding: 8px 16px;
        text-transform: uppercase;
        margin-block-end: 8px;
      }
    }
    .finish_order {
      a {
        background-color: #ffc400;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 8px 16px;
        text-transform: uppercase;
        color: initial;
        margin-block-end: 8px;
      }
    }
  }
}
</style>
<script>
import CartItem from "@/components/subcomponents/subcomponents/cart-item.vue";
export default {
  data: () => {
    return {
      show: false,
    };
  },
  components: {
    CartItem,
  },
};
</script>
