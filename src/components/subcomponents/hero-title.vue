!
<template>
  <div class="hero_title">
    <div v-if="title" class="title">{{ title }}</div>
    <span v-if="subtitle" class="subtitle">{{ subtitle }}</span>
  </div>
</template>
<style lang="scss" scoped>
.hero_title {
  margin-block-end: 64px;
  .title {
    font-size: 32px;
    font-weight: bold;
    text-transform: uppercase;
    text-shadow: #51ffe4 4px 7px 0px;
    margin-inline: auto;
    margin-block-start: 64px;
    display: block;
    width: fit-content;
  }
  .subtitle {
    font-size: 16px;
    text-transform: uppercase;
    display: block;
    text-align: center;
    width: fit-content;
    margin-inline: auto;
    margin-block-end: 64px;
  }
}
@media screen and (max-width: 768px) {
  .hero_title {
    margin-block-end: 8px;
    .title {
      text-shadow: #51ffe4 2px 3px 0px;
    }
    .subtitle {
      margin-block-end: 0px;
    }
  }
}
</style>
<script>
export default {
  props: ["title", "subtitle"],
};
</script>
