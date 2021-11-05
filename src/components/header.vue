<template>
  <div class="header">
    <nav class="navbar navbar-expand-lg navbar-light bg-white shadow">
      <div class="container">
        <router-link to="#" class="navbar-brand">
          <img class="logo" src="@/assets/luxystyle-logo.svg" alt="logo" />
        </router-link>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarText"
          aria-controls="navbarText"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarText">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0 text-uppercase center-nav">
            <li class="nav-item">
              <router-link to="#" class="nav-link">Accueil</router-link>
            </li>
            <li class="nav-item">
              <router-link to="#" class="nav-link">Boutique</router-link>
            </li>
            <li class="nav-item">
              <router-link to="#" class="nav-link">à proppos</router-link>
            </li>
            <li class="nav-item">
              <router-link to="#" class="nav-link">Contact</router-link>
            </li>
          </ul>
          <ul class="navbar-nav ms-auto mb-2 mb-lg-0 text-uppercase end-nav">
            <li class="nav-item">
              <router-link to="#" class="nav-link">
                <i class="bi bi-search"></i>
              </router-link>
            </li>
            <li class="nav-item">
              <router-link to="#" class="nav-link">
                <span class="cart-icon">
                  <i class="bi bi-bag"></i>
                  <span class="cart-count">0</span>
                </span>
              </router-link>
            </li>
            <li class="nav-item">
              <router-link to="#" class="nav-link">
                <i class="bi bi-truck"></i>
              </router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <FixedCart />
  </div>
</template>
<style lang="scss" scoped>
.header {
  min-height: 60px;
  position: sticky;
  top: 0px;
  z-index: 99;
}
.nav.navbar {
  padding: 0px;
}
a.nav-link {
  transition: 0.3s;
}
a.nav-link:hover {
  text-shadow: #51ffe4 2px 2px 0px;
  transform: translateY(-2px);
}
.navbar-nav {
  font-size: 16px;
}
.logo {
  max-height: 50px;
  max-width: 130px;
}
.cart-icon {
  position: relative;
  .cart-count {
    text-shadow: none !important;
    position: absolute;
    right: -5px;
    bottom: -5px;
    color: rgb(255, 255, 255);
    background: red;
    border-radius: 15px;
    font-weight: bold;
    height: 15px;
    width: 15px;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    font-size: 9px;
  }
}
@media screen and (max-width: 768px) {
  .end-nav {
    flex-direction: row;
    justify-content: space-around;
  }
}
</style>
<script>
import FixedCart from "@/components/subcomponents/fixed-cart.vue";
export default {
  components: {
    FixedCart,
  },
};
</script>
