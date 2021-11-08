<template>
  <div class="dirct_checkout">
    <Header />
    <div class="container">
      <div class="row py-5">
        <div class="col-md-7 py-3">
          <div class="form">
            <form>
              <div class="row">
                <div class="form-group col-md-6">
                  <label for="name"
                    >Nom complet(<span class="text-danger">*</span>):</label
                  >
                  <input
                    id="name"
                    type="text"
                    placeholder="Tapez votre nom et prénom..."
                    class="form-control"
                  />
                </div>
                <div class="form-group col-md-6">
                  <label for="phone"
                    >Téléphone(<span class="text-danger">*</span>):</label
                  >
                  <input
                    id="phone"
                    type="text"
                    placeholder="Tapez votre numero de téléphone..."
                    class="form-control"
                  />
                </div>
              </div>
              <div class="row">
                <div class="form-group col-md-6">
                  <label for="city"
                    >Ville(<span class="text-danger">*</span>):</label
                  >
                  <input
                    id="city"
                    type="text"
                    placeholder="Tapez votre nom et prénom..."
                    class="form-control"
                  />
                </div>
                <div class="form-group col-md-6">
                  <label for="adress"
                    >Adresse(<span class="text-danger">*</span>):</label
                  >
                  <input
                    id="adress"
                    type="text"
                    placeholder="Tapez votre adresse..."
                    class="form-control"
                  />
                </div>
              </div>
              <div class="form-group">
                <label for="message">Message:</label>
                <textarea
                  placeholder="Tapez votre message..."
                  id="message"
                  cols="15"
                  rows="5"
                  class="form-control"
                ></textarea>
              </div>
              <span class="helper mb-2 d-block"
                >les champs avec le signe (<span class="text-danger">*</span>)
                sont obligatoires</span
              >
            </form>
          </div>
        </div>
        <div class="col-md-5 shadow border py-3 bg-light">
          <CartItem class="card_item" />
          <div class="product">
            <div class="title">Prix du produit x 3</div>
            <div class="price">3988.00DH</div>
          </div>
          <div class="form-group p-2 border-success border mb-3 bg-warning">
            <span class="h4 d-block">Méthode de livraison:</span>
            <input checked type="radio" id="cod" />
            <label for="cod" class="form-chack-label"
              >Paiement à la livraison</label
            >
          </div>
          <div class="shipping">
            Livraison
            <div class="title"></div>
            <div class="price">50DH</div>
          </div>
          <div class="total_order">
            <div class="title">Total de la commande</div>
            <div class="price">95699.99DH</div>
          </div>
          <div class="finishorder">
            <button class="btn btn-primary">confirmez</button>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>
<style lang="scss" scoped>
.dirct_checkout {
  .card_item {
    border: 1px solid #04ac92;
    background-color: #04ac931a;
    padding: 16px 8px;
    margin-block-end: 32px;
  }
  .form {
    form {
      .form-group {
        margin-block-end: 16px;
        label {
          font-size: 14px;
          margin-block-end: 4px;
        }
        .form-control {
          border-radius: 0px;
          border: 1px solid #04ac92;
          background-color: #f7f8fa;
          padding-block: 8px;
          padding-inline: 16px;
          &::placeholder {
            opacity: 0.7;
          }
        }
        .file {
          position: relative;
          height: 40px;
          label {
            position: absolute;
            inset-inline: 0;
            inset-block: 0;
            margin: 0;
            padding: 0;
            z-index: 1;
            background-color: #51ffe4;
            opacity: 1;
            display: flex;
            justify-content: flex-start;
            align-items: center;
            padding-inline-end: 16px;
            cursor: pointer;
            transition: 0.3s;
            i {
              margin-inline-end: 8px;
              font-size: 18px;
              height: 100%;
              width: 50px;
              background-color: rgba(0, 0, 0, 0.37);
              display: flex;
              justify-content: center;
              align-items: center;
              color: #ffffff;
            }
            &:hover {
              background-color: #04ac92;
            }
          }
          input {
            position: absolute;
            inset-inline: 0;
            inset-block: 0;
            margin: 0;
            padding: 0;
          }
        }
        button {
          &[type="submit"] {
            border-radius: 0px;
            background-color: #04ac92;
            color: #ffffff;
            font-weight: bold;
            font-size: 21px;
            display: flex;
            justify-content: center;
            align-items: center;
            border-color: #04ac92;
            width: 100%;
            height: 56px;
            &:hover {
              box-shadow: #04ac933f 0px 6px 8px;
            }
          }
        }
        .stars {
          i {
            color: #ff6f00;
            margin-inline-end: 4px;
            font-size: 18px;
          }
        }
      }
    }
  }
  .total_order {
    display: flex;
    justify-content: space-between;
    font-size: 24px;
    font-weight: bold;
    margin-block-end: 16px;
    .title {
    }
    .price {
      color: red;
    }
  }
  .shipping {
    display: flex;
    justify-content: space-between;
    font-size: 18px;
    margin-block-end: 16px;
    .title {
    }
    .price {
      color: #04ac92;
    }
  }
  .product {
    display: flex;
    justify-content: space-between;
    font-size: 18px;
    margin-block-end: 16px;
    .title {
    }
    .price {
      color: #04ac92;
    }
  }
  button {
    text-transform: uppercase;
    border-radius: 0px;
    background-color: #ffffff;
    color: #04ac92;
    border-radius: 8px;
    font-weight: bold;
    font-size: 21px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-color: #04ac92;
    width: 100%;
    height: 56px;
    &:hover {
      box-shadow: #04ac933f 0px 6px 8px;
      background-color: #04ac92;
      color: #ffffff;
    }
  }
}
@media screen and (max-width: 768px) {
  .dirct_checkout {
    .card_item {
    }
    .form {
      form {
        .form-group {
          label {
          }
          .form-control {
            &::placeholder {
            }
          }
          .file {
            label {
              i {
              }
            }
            input {
            }
          }
        }
      }
    }
    .total_order {
      font-size: 20px;
      .title {
      }
      .price {
      }
    }
    .shipping {
      .title {
      }
      .price {
      }
    }
    .product {
      .title {
      }
      .price {
      }
    }
    button {
    }
  }
}
</style>
<script>
import Header from "@/components/header.vue";
import Footer from "@/components/footer.vue";
import CartItem from "@/components/subcomponents/subcomponents/cart-item.vue";
export default {
  components: {
    Header,
    CartItem,
    Footer,
  },
};
</script>
