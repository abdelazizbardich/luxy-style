<template>
  <div v-if="title" class="page_title">{{ title }}</div>
</template>
<style lang="scss" scoped>
.page_title {
  height: 150px;
  width: 100%;
  background-color: #04ac92;
  font-size: 54px;
  color: #ffffff;
  text-transform: uppercase;
  display: flex;
  justify-content: center;
  align-items: center;
  font-weight: bold;
}
@media screen and (max-width: 768px) {
  .page_title {
    font-size: 32px;
    height: 70px;
  }
}
</style>
<script>
export default {
  props: ["title"],
};
</script>
