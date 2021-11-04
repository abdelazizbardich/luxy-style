<template>
  <div class="instagram_post">
    <div class="thumbnail">
      <img src="@/assets/instagram.png" alt="instagram post" />
      <span class="overlay"><i class="bi bi-instagram"></i></span>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.instagram_post {
  padding: 8px;
  cursor: pointer;
  .thumbnail {
    width: 100%;
    position: relative;
    img {
      width: 100%;
    }
    &:hover {
      .overlay {
        opacity: 1;
      }
    }
    .overlay {
      transition: 0.3s;
      opacity: 0;
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #04ac9385;
      color: #ffffff;
      font-size: 64px;
    }
  }
}
</style>
<script>
export default {};
</script>
