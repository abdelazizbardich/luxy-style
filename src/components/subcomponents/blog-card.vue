<template>
  <div class="blog_card">
    <div class="thumbnail">
      <img src="@/assets/blog.png" alt="blog thumbnail" />
    </div>
    <div class="details">
      <span class="category">La mode</span>
      <span class="title">DOLORE EU FUGIATNULLA PARIATUR</span>
      <p class="snipet">
        Lorem ipsum dolor sit amet conse ctetur adipisicing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua.
      </p>
      <div class="infos">
        <span
          >Par <span class="author">Admin</span> le
          <span class="date">14 janvier 2017</span>
        </span>
        <span class="comments"
          ><i class="bi bi-chat"></i><span class="count">1</span></span
        >
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.blog_card {
  padding: 4px;
  margin-block-end: 16px;
  .thumbnail {
    position: relative;
    border: 10px solid #ffffff;
    &::after {
      content: "";
      position: absolute;
      top: 25%;
      left: 0;
      right: 0;
      bottom: 0;
      background-image: linear-gradient(transparent, #016051);
    }
    img {
      width: 100%;
    }
  }
  .details {
    border: 3px solid #51ffe4;
    border-radius: 32px 32px 0px 0px;
    padding: 16px;
    max-width: 90%;
    margin-inline: auto;
    background-color: #ffffff;
    margin-top: -30%;
    position: relative;
    z-index: 1;
    .category {
      font-size: 12px;
      text-transform: uppercase;
      color: #04ac92;
      display: block;
      margin: auto;
      width: fit-content;
      margin-block-end: 16px;
    }
    .title {
      font-size: 20px;
      text-transform: uppercase;
      display: block;
      margin: auto;
      width: fit-content;
      margin-block-end: 16px;
      font-weight: bold;
      text-align: center;
    }
    .snipet {
      font-size: 12px;
      display: block;
      margin: auto;
      width: 90%;
      margin-block-end: 16px;
      text-align: center;
    }
    .infos {
      font-size: 10px;
      text-align: center;
      display: flex;
      align-items: center;
      justify-content: center;
      .author {
        font-weight: bold;
      }
      .comments {
        margin-inline-start: 16px;
        position: relative;
        width: fit-content;
        height: fit-content;
        color: #04ac92;
        font-size: 20px;
        .count {
          color: initial;
          font-size: 12px;
          position: absolute;
          left: 50%;
          top: 50%;
          transform: translate(-50%, -50%);
        }
      }
    }
  }
}
</style>
<script>
export default {};
</script>
