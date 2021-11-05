<template>
  <div class="card_item">
    <div v-if="icon" class="icon">
      <i :class="icon"></i>
    </div>
    <div v-if="title" class="details">
      <div v-if="title" class="title">{{ title }}</div>
      <div v-if="description" class="description" v-html="description"></div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["icon", "title", "description"],
};
</script>
<style lang="scss" scoped>
.card_item {
  padding: 16px 32px;
  border: 5px solid #c1faf1;
  margin: 8px;
  display: flex;
  align-items: center;
  box-shadow: #41b8a652 0px 6px 8px;
  background-color: #ffffff;
  .icon {
    i {
      color: #04ac92;
      font-size: 32px;
      margin-inline-end: 16px;
    }
  }
  .details {
    .title {
      color: #04ac92;
      font-size: 16px;
      text-transform: uppercase;
    }
    .description {
      font-size: 14px;
    }
  }
}
@media screen and (max-width: 768px) {
  .card_item {
    flex-direction: column;
    text-align: center;
    padding: 5px;
    margin-inline: 4px;
    margin-block-end: 8px;
    .icon {
      text-align: center;
      i {
        margin: 0px;
      }
    }
    .details {
      .title {
        font-size: 12px;
      }
      .description {
      }
    }
  }
}
</style>
