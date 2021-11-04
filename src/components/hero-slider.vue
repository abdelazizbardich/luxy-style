<template>
  <div class="hero_slider">
    <div class="container">
      <div class="row">
        <div class="col-md-7 order-2 order-md-1">
          <div class="slider_category">
            <span class="category_text">Hight tech -> Pc</span>
            <span class="stars">
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
            </span>
          </div>
          <span class="slider_title">
            Ordinateur portable Apple MacBook air 13,3 "
          </span>
          <p class="slider_description">
            Apple Ordinateur portable MacBook Air 13,3 pouces avec Touch ID
            Intel Core i3 8 Go de mémoire Disque SSD 256 Go (dernier modèle)
            Gris sidéral
          </p>
          <div class="slider_action">
            <span class="price">999.99DH</span>
            <router-link to="#" class="slider_order">Commandez</router-link>
          </div>
        </div>
        <div class="col-md-5 order-1 order-md-2">
          <img
            class="slider_image"
            src="@/assets/laptop.png"
            alt="slider image"
          />
        </div>
        <span @click="scrollDown" class="slider_scroll_down">
          <i class="bi bi-arrow-down-short"></i>
        </span>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.hero_slider {
  width: 100%;
  height: calc(100vh - 61px);
  position: relative;
  background-image: linear-gradient(90deg, transparent 50%, #c1faf1 50%);
  display: flex;
  align-items: center;
  .slider_image {
    max-width: 100%;
    width: 618px;
  }
  .slider_category {
    margin-inline-start: auto;
    box-shadow: #41d6bf 0px 3px 8px;
    height: fit-content;
    width: fit-content;
    padding: 8px 16px;
    border-radius: 8px;
    background-color: #51ffe4;
    position: relative;
    &::before {
      content: "";
      position: absolute;
      width: 50vw;
      height: 5px;
      top: 50%;
      left: 0;
      z-index: -1;
      transform: translateX(-100%) translateY(-50%);
      background-color: #51ffe4;
    }
    &::after {
      content: "";
      position: absolute;
      height: 30px;
      width: 30px;
      border-radius: 30px;
      background-color: #51ffe4;
      left: calc(-100vh + 37%);
      top: 50%;
      transform: translateY(-50%);
    }
    .category_text {
      margin-inline-end: 16px;
    }
    .stars {
      i {
        color: #ff0033;
        margin-inline: 2px;
      }
    }
  }
  .slider_title {
    font-size: 64px;
    text-transform: uppercase;
    font-weight: bold;
    text-align: right;
    text-shadow: #51ffe4 4px 7px 0px;
    // max-width: 634px;
    display: block;
    margin-inline-start: auto;
  }
  .slider_description {
    font-size: 24px;
  }
  .slider_action {
    display: flex;
    margin-inline-start: auto;
    width: fit-content;
    align-items: center;
    .price {
      font-size: 32px;
      color: #04ac92;
      font-weight: bold;
      text-transform: uppercase;
      margin-inline-end: 16px;
    }
    .slider_order {
      font-size: 16px;
      color: #04ac92;
      font-weight: bold;
      text-transform: uppercase;
      margin-inline-end: 8px;
      background-color: #ffffff;
      padding: 8px 16px;
      border: 2px solid #04ac92;
      border-inline-start-width: 15px;
    }
  }
  .slider_scroll_down {
    height: 40px;
    width: 40px;
    border-radius: 40px;
    background: #ffffff;
    display: flex;
    position: absolute;
    left: 50%;
    bottom: 15px;
    justify-content: center;
    align-items: center;
    color: #04ac92;
    font-size: 24px;
    transform: translateX(-50%);
    box-shadow: #49dbc4 0px 7px 12px;
    transition: 0.5s;
    cursor: pointer;
    i {
      animation: slider_scroll_down ease-in-out 2s infinite;
      display: block;
    }
    &:hover {
      box-shadow: #49dbc4 0px 12px 24px;
      transform: translateX(-50%) scale(1.1);
    }
  }
}
@keyframes slider_scroll_down {
  0% {
    transform: translateY(-10px);
    opacity: 0;
  }
  50% {
    transform: translateY(5px);
    opacity: 1;
  }
  100% {
    transform: translateY(10px);
    opacity: 0;
  }
}
@media screen and (max-width: 992px) {
  .hero_slider {
    .slider_title {
      font-size: 32px;
      text-align: start;
      margin-bottom: 16px;
    }
    .slider_description {
      font-size: 14px;
      margin-bottom: 16px;
    }
    .slider_image {
      max-width: 60%;
      width: 618px;
      margin: auto;
      display: block;
    }
    .slider_action {
      flex-direction: column;
      margin: auto;
    }
    .slider_category {
      margin-inline-end: auto;
      margin-inline-start: initial;
    }
    .slider_scroll_down {
      display: none;
    }
    .slider_category {
      padding: 5px 8px;
      font-size: 14px;
    }
  }
}
</style>
<script>
export default {
  methods: {
    scrollDown() {
      window.scrollTo(0, window.innerHeight - 70);
    },
  },
};
</script>
