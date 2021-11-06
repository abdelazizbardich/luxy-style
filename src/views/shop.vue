<template>
  <div class="shop">
    <Header />
    <PageTitle :title="'Boutique'" />
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="filter">
            <form class="row m-0">
              <div class="form-group m-0 col-md-2">
                <label>Prix minimum(dh):</label>
                <input type="text" value="0" class="form-control" />
              </div>
              <div class="form-group m-0 col-md-2">
                <label>Prix max(dh):</label>
                <input type="text" value="1000" class="form-control" />
              </div>
              <div class="form-group m-0 col-md">
                <label>Categorie:</label>
                <select class="form-control form-select">
                  <option value="" selected disabled>Categorie</option>
                  <option value="opt">Option</option>
                </select>
              </div>
              <div class="form-group m-0 col-md-auto">
                <label>Numérotation des pages:</label>
                <ul class="paggination">
                  <li class="prev"><i class="bi bi-arrow-left"></i></li>
                  <li class="page_number"><span>1</span></li>
                  <li class="page_number"><span>2</span></li>
                  <li class="page_number"><span>3</span></li>
                  <li class="page_number active"><span>4</span></li>
                  <li class="page_number"><span>5</span></li>
                  <li class="page_number"><span>6</span></li>
                  <li class="next"><i class="bi bi-arrow-right"></i></li>
                </ul>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>
<style lang="scss" scoped>
.filter {
  padding-block: 16px;
  width: 100%;
  background-color: #04ac92;
  margin-block-end: 16px;
  form {
    display: flex;
    justify-content: center;
    align-items: center;
    .form-group {
      label {
        color: #ffffff;
        margin-block-end: 8px;
      }
      .paggination {
        list-style: none;
        display: flex;
        align-items: center;
        justify-content: flex-start;
        margin: 0px;
        padding: 0px;
        li {
          transition: 0.3s;
          cursor: pointer;
          &:hover {
            transform: scale(1.1);
          }
          &.active {
            span {
              width: 25px;
              height: 25px;
              border-radius: 25px;
              background-color: #04ac92;
              margin: 2px;
              text-align: center;
              font-size: 15px;
              display: flex;
              justify-content: center;
              align-items: center;
              border: 2px solid #ffffff;
              color: #ffffff;
            }
          }
          span {
            width: 25px;
            height: 25px;
            border-radius: 25px;
            background-color: #ffffff;
            margin: 2px;
            text-align: center;
            font-size: 15px;
            display: flex;
            justify-content: center;
            align-items: center;
          }
          &.prev {
            width: 30px;
            height: 30px;
            border-radius: 30px;
            color: #ffffff;
            background-color: #027563;
            margin: 2px;
            text-align: center;
            font-size: 15px;
            display: flex;
            justify-content: center;
            align-items: center;
          }
          &.next {
            width: 30px;
            height: 30px;
            border-radius: 30px;
            color: #ffffff;
            background-color: #027563;
            margin: 2px;
            text-align: center;
            font-size: 15px;
            display: flex;
            justify-content: center;
            align-items: center;
          }
        }
      }
    }
  }
}
</style>
<script>
import Header from "@/components/header.vue";
import Footer from "@/components/footer.vue";
import PageTitle from "@/components/page-title.vue";
export default {
  components: {
    Header,
    Footer,
    PageTitle,
  },
};
</script>
