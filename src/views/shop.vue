<template>
  <div class="shop">
    <Header />
    <PageTitle :title="'Boutique'" />
    <div class="container filter">
      <div class="row">
        <div class="col-12">
          <form class="row m-0">
            <div class="form-group m-0 col-3 col-md-2">
              <label>Prix mini(dh):</label>
              <input min="0" type="number" value="0" class="form-control" />
            </div>
            <div class="form-group m-0 col-3 col-md-2">
              <label>Prix max(dh):</label>
              <input min="10" type="number" value="1000" class="form-control" />
            </div>
            <div class="form-group m-0 col-6 col-md">
              <label>Categorie:</label>
              <select class="form-control form-select">
                <option value="" selected disabled>Categorie</option>
                <option value="categorie">Categorie...</option>
              </select>
            </div>
            <div class="form-group m-0 col-12 col-md-auto">
              <label>Numérotation des pages:</label>
              <ul class="paggination">
                <li class="prev"><i class="bi bi-arrow-left"></i></li>
                <li class="page_number">
                  <router-link to="#"><span>1</span></router-link>
                </li>
                <li class="page_number">
                  <router-link to="#"><span>2</span></router-link>
                </li>
                <li class="page_number">
                  <router-link to="#"><span>3</span></router-link>
                </li>
                <li class="page_number active">
                  <router-link to="#"><span>4</span></router-link>
                </li>
                <li class="page_number">
                  <router-link to="#"><span>5</span></router-link>
                </li>
                <li class="page_number">
                  <router-link to="#"><span>6</span></router-link>
                </li>
                <li class="next"><i class="bi bi-arrow-right"></i></li>
              </ul>
            </div>
          </form>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-12">
          <ShopGrid />
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
  margin-block-end: 32px;
  position: sticky;
  top: 59px;
  z-index: 9;
  box-shadow: #2ead9a96 0px 5px 32px;
  form {
    display: flex;
    justify-content: center;
    align-items: center;
    .form-group {
      label {
        color: #ffffff;
        margin-block-end: 8px;
      }
      .form-control {
        border: none;
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
          a {
            color: initial;
          }
          &:hover {
            transform: scale(1.1);
          }
          &.active {
            &:hover {
              transform: scale(1);
            }
            span {
              cursor: initial;
              user-select: none;
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
@media screen and (max-width: 768px) {
  .filter {
    padding-block: 8px;
    form {
      .form-group {
        label {
          font-size: 10px;
          margin-bottom: 4px;
        }
        .form-control {
          padding: 4px 8px;
        }
        .paggination {
          li {
            a {
            }
            &:hover {
            }
            &.active {
              &:hover {
              }
              span {
              }
            }
            span {
            }
            &.prev {
            }
            &.next {
            }
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
import ShopGrid from "@/components/shop-grid.vue";
export default {
  components: {
    Header,
    Footer,
    PageTitle,
    ShopGrid,
  },
};
</script>
