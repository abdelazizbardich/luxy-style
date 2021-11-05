<template>
  <div class="cart_item">
    <div class="container-fluid">
      <div class="row">
        <div class="col-auto thumbnail">
          <img src="@/assets/cart.png" alt="cart item" />
        </div>
        <div class="col">
          <span class="title">Apple - MacBook air 13.3" Laptop</span>
          <span class="price"
            >{{ qte }} x {{ price }}DH
            <span class="counter">
              <input v-model="qte" class="number" type="number" />
              <span>
                <button @click="up" class="up">
                  <i class="bi bi-caret-up-fill"></i>
                </button>
                <button @click="down" class="down">
                  <i class="bi bi-caret-down-fill"></i>
                </button>
              </span>
            </span>
          </span>
        </div>
        <div class="col-auto close"><i class="bi bi-x-circle-fill"></i></div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.cart_item {
  margin-block-end: 8px;
  .thumbnail {
    img {
      width: 70px;
      height: 70px;
      border: 1px solid #c1faf1;
      background-color: #ffffff;
    }
  }
  .title {
    color: #04ac92;
    font-size: 14px;
    text-transform: uppercase;
    font-weight: bold;
    display: block;
  }
  .price {
    font-size: 14px;
    font-weight: bold;
    display: block;
    text-transform: uppercase;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .counter {
      display: flex;
      border: 1px solid #c1faf1;
      .number {
        height: 24px;
        width: 24px;
        border: none;
        text-align: center;
        font-weight: bold;
        background-color: #ffffff;
        &::-webkit-inner-spin-button,
        &::-webkit-outer-spin-button {
          display: none;
        }
      }
      .up {
        width: 12px;
        height: 12px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 8px;
        background-color: #04ac92;
        &:hover {
          background-color: #028874;
        }
        color: #ffffff;
        border: none;
      }
      .down {
        width: 12px;
        height: 12px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 8px;
        background-color: #04ac92;
        &:hover {
          background-color: #028874;
        }
        color: #ffffff;
        border: none;
      }
    }
  }
  .close {
    i {
      cursor: pointer;
      transition: 0.3s;
      display: inline-block;
      &:hover {
        color: #04ac92;
      }
    }
  }
}
</style>
<script>
export default {
  data: () => {
    return {
      qte: 0,
      price: 999.99,
    };
  },
  methods: {
    up() {
      this.qte++;
    },
    down() {
      this.qte--;
    },
  },
};
</script>
