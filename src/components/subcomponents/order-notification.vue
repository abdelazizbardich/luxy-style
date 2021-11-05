<template>
  <div
    class="order_notification"
    :style="!show ? 'transform: translateY(200%);' : ''"
  >
    <div class="thumbnail">
      <img src="@/assets/cart.png" alt="order photo" />
    </div>
    <div class="details">
      <span class="tag">Quelqu'un a commandé:</span>
      <span class="title">Apple - MacBook air 13.3" Laptop</span>
      <span class="footer">
        <span class="price">10999.99DH</span>
        <span class="date">il y a 1 minute</span>
      </span>
      <div @click="close" class="close"><i class="bi bi-x"></i></div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.order_notification {
  display: flex;
  justify-content: stretch;
  align-items: center;
  border-radius: 10px;
  border: 1px solid #51ffe4;
  background: #ffffff;
  position: fixed;
  left: 25px;
  bottom: 25px;
  width: 300px;
  padding: 8px 16px;
  box-shadow: #49dbc570 0px 11px 17px;
  transition: 0.3s;
  .thumbnail {
    width: 70px;
    img {
      border-radius: 5px;
      width: 100%;
    }
    margin-inline-end: 16px;
  }
  .details {
    .tag {
      font-size: 12px;
      display: block;
    }
    .title {
      font-size: 12px;
      font-weight: bold;
      color: #04ac92;
      display: block;
    }
    .footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      .price {
        font-size: 12px;
        font-weight: bold;
      }
      .date {
        font-size: 10px;
      }
    }
    .close {
      position: absolute;
      inset-block-start: 5px;
      inset-inline-end: 5px;
      i {
        color: #ff0000;
        font-size: 16px;
        cursor: pointer;
      }
    }
  }
}
</style>
<script>
export default {
  data: () => {
    return {
      show: false,
    };
  },
  mounted() {
    var audio = new Audio(require("@/assets/sounds/order-notification.flac"));
    audio.play();
    this.show = true;
  },
  methods: {
    close() {
      this.show = false;
    },
  },
};
</script>
