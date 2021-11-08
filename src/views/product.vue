<template>
  <div class="product">
    <Header />
    <PageTitle class="page_title" :title="'Produit'" />
    <div class="container presentation">
      <div class="row">
        <div class="col-md-6">
          <div class="path">
            <router-link to="/">Accueil</router-link> >
            <router-link to="/boutique">Boutique</router-link> >
            <span>Product name</span>
          </div>
          <div class="thumbnail">
            <img :src="activeSlide.path" :alt="activeSlide.title" />
          </div>
          <div class="gallery">
            <div class="gallery_item">
              <img
                @click="setActiveSlide(1)"
                src="@/assets/gallery-1.png"
                alt="products gallery"
              />
            </div>
            <div class="gallery_item">
              <img
                @click="setActiveSlide(2)"
                src="@/assets/gallery-2.png"
                alt="products gallery"
              />
            </div>
            <div class="gallery_item">
              <img
                @click="setActiveSlide(3)"
                src="@/assets/gallery-3.png"
                alt="products gallery"
              />
            </div>
            <div class="gallery_item">
              <img
                @click="setActiveSlide(4)"
                src="@/assets/gallery-4.png"
                alt="products gallery"
              />
            </div>
            <div class="gallery_item">
              <img
                @click="setActiveSlide(5)"
                src="@/assets/gallery-5.png"
                alt="products gallery"
              />
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <div class="title">Ordinateur portable Apple MacBook air 13,3 "</div>
          <div class="description">
            <p>
              Apple - Ordinateur portable MacBook Air 13,3 pouces avec Touch ID
              - Intel Core i3 - 8 Go de mémoire - Disque SSD 256 Go (dernier
              modèle) - Gris sidéral
            </p>
          </div>
          <div class="infos">
            <div class="price">999.99dh</div>
            <div class="old_price">
              <span>24500Dh</span><span class="reduction">-45%</span>
            </div>
            <div class="stars">
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star"></i>
            </div>
          </div>
          <div class="qte">
            <span class="title">Quantité</span>
            <div class="controller">
              <button @click="down" class="down">
                <i class="bi bi-dash"></i>
              </button>
              <span>{{ qte }}</span>
              <button @click="up" class="up">
                <i class="bi bi-plus"></i>
              </button>
            </div>
          </div>
          <div class="stock">
            <span class="title">Seulement 594 restant en stock</span>
            <div class="progress">
              <div
                class="progress-bar"
                role="progressbar"
                aria-valuenow="70"
                aria-valuemin="0"
                aria-valuemax="100"
                style="width: 70%"
              >
                <span class="sr-only">70% Complete</span>
              </div>
            </div>
          </div>
          <div class="actions">
            <div class="order_now">Acheter maintenant</div>
            <div class="add_to_cart">Ajouter au panier</div>
          </div>
          <div class="share">
            <span class="icon"><i class="bi bi-share-fill"></i></span>
            <a href="#"><i class="bi bi-facebook"></i></a>
            <a href="#"><i class="bi bi-twitter"></i></a>
            <a href="#"><i class="bi bi-instagram"></i></a>
            <a href="#"><i class="bi bi-pinterest"></i></a>
          </div>
        </div>
      </div>
    </div>
    <div class="container description">
      <div class="row">
        <div class="col-12">
          <div class="title">Détails du produit:</div>
          <div class="content">
            <p>
              Pellentesque commodo eros a enim. Sed magna purus, fermentum eu,
              tincidunt eu, varius ut, felis. Duis vel nibh at velit scelerisque
              suscipit. Praesent ut ligula non mi varius sagittis. Nulla sit
              amet est.
            </p>
            <img
              style="width: 100%; margin-block-end: 16px"
              src="@/assets/product-details.jpg"
              alt=""
            />
            <p>
              Pellentesque commodo eros a enim. Sed magna purus, fermentum eu,
              tincidunt eu, varius ut, felis. Duis vel nibh at velit scelerisque
              suscipit. Praesent ut ligula non mi varius sagittis. Nulla sit
              amet est. Aenean vulputate eleifend tellus. Cras varius. Aenean
              tellus metus, bibendum sed, posuere ac, mattis non, nunc. Donec
              quam felis, ultricies nec, pellentesque eu, pretium quis, sem.
              Aenean posuere, tortor sed cursus feugiat, nunc augue blandit
              nunc, eu sollicitudin urna dolor sagittis lacus. In dui magna,
              posuere eget, vestibulum et, tempor auctor, justo. Donec vitae
              sapien ut libero venenatis faucibus. Vestibulum purus quam,
              scelerisque ut, mollis sed, nonummy id, metus. Sed aliquam
              ultrices mauris. Pellentesque auctor neque nec urna. Pellentesque
              dapibus hendrerit tortor. Phasellus accumsan cursus velit. Ut
              tincidunt tincidunt erat. Vestibulum purus quam, scelerisque ut,
              mollis sed, nonummy id, metus. Phasellus volutpat, metus eget
              egestas mollis, lacus lacus blandit dui, id egestas quam mauris ut
              lacus. Class aptent taciti sociosqu ad litora torquent per conubia
              nostra, per inceptos hymenaeos. Donec mollis hendrerit risus.
              Aenean ut eros et nisl sagittis vestibulum. Cras dapibus. Etiam
              iaculis nunc ac metus.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="container reviews">
      <div class="row">
        <div class="col-md-12">
          <div class="title">Évaluations et commentaires:</div>
        </div>
        <div class="col-md-auto review">
          <div class="numbers">5.0/5</div>
          <div class="stars">
            <i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i
            ><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i
            ><i class="bi bi-star"></i>
          </div>
          <div class="reviews_count">6 évaluations</div>
        </div>
      </div>
    </div>
    <div class="container comments">
      <div class="row">
        <div class="col-12">
          <div class="title">Avis sur le produit:</div>
        </div>
        <div class="col-12">
          <div class="comment" v-for="(i, index) in 5" :key="index">
            <div class="header">
              <span class="author">Par <span class="name">Budark S</span></span>
              <span class="stars"
                ><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i
                ><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i
                ><i class="bi bi-star-fill"></i
              ></span>
              <span class="date">Il y a 2 semaines</span>
            </div>
            <div class="description">
              <p>
                loSed aliquam ultrices mauris. Vestibulum purus quam,
                scelerisque ut, mollis sed, nonummy id, metus. Maecenas
                vestibulum mollis diam. Etiam rhoncus. Etiam rhoncus.
              </p>
            </div>
            <div class="photos">
              <div class="photo">
                <img src="@/assets/product.png" alt="review img" />
              </div>
              <div class="photo">
                <img src="@/assets/product.png" alt="review img" />
              </div>
              <div class="photo">
                <img src="@/assets/product.png" alt="review img" />
              </div>
              <div class="photo">
                <img src="@/assets/product.png" alt="review img" />
              </div>
              <div class="photo">
                <img src="@/assets/product.png" alt="review img" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container add_comment">
      <div class="row">
        <div class="col-md-12">
          <div class="title">Écrivez Une Avis</div>
        </div>
        <div class="col-md-12">
          <div class="form">
            <form action="">
              <div class="form-group">
                <label for="name">Nom</label>
                <input
                  required
                  type="text"
                  placeholder="Tapez votre nom..."
                  id="name"
                  class="form-control"
                />
              </div>
              <div class="form-group">
                <label for="comment">Avis:</label>
                <textarea
                  placeholder="Tapez votre avis..."
                  required
                  id="comment"
                  cols="30"
                  rows="10"
                  class="form-control"
                ></textarea>
              </div>
              <div class="form-group">
                <label for="stars"
                  >Combien d'étoiles pouvez-vous attribuer à ce produit?</label
                >
                <div class="stars">
                  <i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i
                  ><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i
                  ><i class="bi bi-star-fill"></i>
                </div>
              </div>
              <div class="form-group">
                <label for="photos">Quelques photos du produit:</label>
                <div class="file">
                  <label for="photos" class="placeholder"
                    ><i class="bi bi-camera"></i> Choisissez quelques
                    photos...</label
                  >
                  <input
                    required
                    type="file"
                    id="photos"
                    multiple
                    accept="image/*"
                    class="form-control"
                  />
                </div>
              </div>
              <div class="form-group">
                <button type="submit" class="btn btn-primary">
                  Soumettre Une avis
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
    <div class="container form_same_category">
      <div class="row">
        <div class="col-12"><div class="title">De la même catégorie:</div></div>
        <div class="grid">
          <productCard v-for="(i, index) in 4" :key="index" />
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>
<style lang="scss" scoped>
.product {
  .presentation {
    padding-block: 32px;
    .path {
      margin-block-end: 8px;
      a {
        color: initial;
        font-size: 14px;
      }
    }
    .thumbnail {
      img {
        width: 100%;
        border: 3px solid #e9ecef;
      }
    }
    .gallery {
      margin-block: 8px;
      display: flex;
      justify-content: flex-start;
      align-items: center;
      flex-wrap: wrap;
      .gallery_item {
        height: 70px;
        width: 70px;
        margin-inline-end: 4px;
        cursor: pointer;
        transition: 0.1s;
        &:hover {
          box-shadow: #04ac9357 0px 3px 3px;
        }
        img {
          width: 100%;
          height: 100%;
          border: 3px solid #e9ecef;
        }
      }
    }
    .title {
      font-size: 48px;
      color: #04ac92;
      font-weight: bold;
    }
    .infos {
      display: flex;
      align-items: center;
      justify-content: flex-start;
      .price {
        font-size: 34px;
        background-color: #04ac92;
        border-radius: 100px;
        padding-inline: 16px;
        font-weight: bold;
        color: #ffffff;
        margin-inline-end: 8px;
        display: inline-block;
      }
      .old_price {
        span {
          font-size: 20px;
          opacity: 0.4;
          text-decoration: line-through;
          &.reduction {
            margin-inline-start: 8px;
            text-decoration: none;
            color: blue;
            opacity: 1;
          }
        }
      }
      .stars {
        margin-inline-start: 8px;
        i {
          color: #ff6f00;
          margin: 2px;
        }
      }
    }
    .qte {
      margin-block: 16px;
      display: flex;
      align-items: center;
      .title {
        font-size: 18px;
        font-weight: lighter;
        color: initial;
        margin-inline-end: 16px;
      }
      .controller {
        display: flex;
        justify-content: space-between;
        align-items: center;
        .down {
          width: 30px;
          height: 30px;
          border-radius: 30px;
          background-color: #e4e4e4;
          border: none;
          color: #00000073;
          font-weight: bolder;
          margin-inline: 8px;
          font-size: 24px;
          line-height: 30px;
          &:hover {
            transform: scale(1.1);
          }
        }
        .up {
          width: 30px;
          height: 30px;
          border-radius: 30px;
          background-color: #04ac92;
          border: none;
          color: #ffffff;
          font-weight: bolder;
          margin-inline: 8px;
          font-size: 24px;
          line-height: 30px;
          &:hover {
            transform: scale(1.1);
          }
        }
      }
    }
    .stock {
      .title {
        font-size: 24px;
        font-weight: bold;
        color: initial;
      }
      .progress {
        border-radius: 50px;
        height: 20px;
        .progress-bar {
          background-color: #04ac92;
          height: 20px;
          border-radius: 50px;
          .sr-only {
            display: none;
          }
        }
      }
    }
    .actions {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-block-start: 16px;
      .order_now {
        width: 45%;
        height: 50px;
        background-color: #ffe600;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-block-end: 8px;
        cursor: pointer;
        transition: 0.3s;
        &:hover {
          box-shadow: #dbc602 4px 6px 0px;
        }
      }
      .add_to_cart {
        width: 45%;
        height: 50px;
        background-color: #04ac92;
        color: #ffffff;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-block-end: 8px;
        cursor: pointer;
        transition: 0.3s;
        &:hover {
          box-shadow: #51ffe4 4px 6px 0px;
        }
      }
    }
    .share {
      display: flex;
      align-items: center;
      border-radius: 30px;
      height: 30px;
      padding-inline-end: 8px;
      background-color: #e9ecef;
      width: fit-content;
      margin-inline-start: auto;
      margin-block: 32px;
      color: #ff6f00;
      .icon {
        background-color: #04ac92;
        width: 30px;
        height: 30px;
        border-radius: 30px;
        display: inline-block;
        color: #ffffff;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 12px;
        margin-inline-end: 8px;
      }
      a {
        display: inline-block;
        margin-inline: 4px;
        color: initial;
      }
    }
  }
  .description {
    .title {
      background-color: #04ac92;
      font-size: 20px;
      color: #ffffff;
      padding: 16px;
      margin-block-end: 16px;
    }
    .content {
      background-color: #f7f8fa;
      padding: 16px;
      margin-block-end: 16px;
    }
  }
  .reviews {
    padding-block-end: 16px;
    .title {
      background-color: #04ac92;
      font-size: 20px;
      color: #ffffff;
      padding: 16px;
      margin-block-end: 16px;
    }
    .review {
      .numbers {
        font-size: 84px;
        font-weight: bold;
        text-transform: uppercase;
      }
      .stars {
        display: flex;
        justify-content: space-between;
        align-items: center;
        i {
          font-size: 24px;
          color: #ff6f00;
        }
      }
      .reviews_count {
        font-size: 16px;
      }
    }
  }
  .comments {
    margin-block-end: 32px;
    .title {
      color: #04ac92;
      font-size: 24px;
      font-weight: bold;
      border-block: 1px solid #04ac9331;
      margin-block: 16px;
      padding-block: 8px;
    }
    .comment {
      margin-block-end: 8px;
      border-block-end: 1px solid #04ac932c;
      &:last-child {
        border: none;
      }
      .header {
        display: flex;
        align-items: center;
        margin-block-end: 8px;
        .author {
          font-weight: bold;
          font-size: 18px;
          margin-inline-end: 16px;
          .name {
            color: #04ac92;
          }
        }
        .stars {
          i {
            font-size: 12px;
            color: #ff6f00;
            margin-inline-end: 4px;
          }
        }
        .date {
          text-align: end;
          flex: 1;
          float: inline-end;
          font-size: 12px;
        }
      }
      .description {
        font-size: 14px;
        text-align: start;
        margin-block-end: 8px;
      }
      .photos {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        margin-block-end: 8px;
        .photo {
          width: 56px;
          margin-block-end: 4px;
          margin-inline-end: 4px;
          img {
            width: 100%;
            border: 3px solid #f7f8fa;
            cursor: pointer;
            &:hover {
              border-color: #04ac92;
            }
          }
        }
      }
    }
  }
  .add_comment {
    .title {
      height: 56px;
      background-color: #04ac92;
      color: #ffffff;
      font-size: 21px;
      font-weight: bold;
      padding-inline: 16px;
      line-height: 56px;
    }
    .form {
      border: 2px solid #04ac92;
      padding-block-start: 16px;
      margin-block-end: 32px;
      padding: 32px;
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
  .form_same_category {
    .title {
      font-size: 40px;
      font-weight: bold;
      text-transform: uppercase;
      text-shadow: #51ffe4 4px 7px 0px;
      margin-block-end: 16px;
    }
    .grid {
      margin-block-end: 64px;
      display: grid;
      grid-template-columns: repeat(4, 1fr);
    }
  }
}
@media screen and (max-width: 798px) {
  .product {
    .page_title {
      display: none;
    }
    .presentation {
      .path {
        font-size: 10px;
        a {
          font-size: 10px;
        }
      }
      .title {
        font-size: 24px;
      }
      .description {
        p {
          font-size: 14px;
        }
      }
      .infos {
        flex-wrap: wrap;
        .stars {
          margin-block: 8px;
          width: 100%;
          i {
            font-size: 24px;
          }
        }
      }
      .stock {
        .title {
          font-size: 16px;
        }
        .progress {
          height: 14px;
          .progress-bar {
            height: 14px;
          }
        }
      }
      .actions {
        flex-direction: column;
        .add_to_cart {
          font-size: 14px;
          width: 100%;
        }
        .order_now {
          font-size: 14px;
          width: 100%;
        }
      }
      .share {
        width: 100%;
        height: 50px;
        .icon {
          height: 55px;
          width: 55px;
          font-size: 20px;
        }
        a {
          i {
            font-size: 20px;
          }
        }
      }
    }
    .reviews {
      text-align: center;
      .review {
        .stars {
          justify-content: center;
          i {
            margin-inline-end: 4px;
          }
        }
      }
    }
    .add_comment {
      .form {
        padding: 8px;
        .form-group {
          textarea {
            height: 150px;
          }
          .stars {
            i {
              font-size: 35px;
              margin-inline: 6px;
            }
          }
        }
      }
    }
    .form_same_category {
      .title {
        font-size: 24px;
        text-align: center;
      }
      .grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }
  }
}
</style>
<script>
import Header from "@/components/header.vue";
import Footer from "@/components/footer.vue";
import PageTitle from "@/components/page-title.vue";
import productCard from "@/components/subcomponents/product-card.vue";
export default {
  data: () => {
    return {
      qte: 1,
      activeSlide: {
        title: "ptoduct thumbnail",
        path: require("@/assets/product-img.png"),
      },
    };
  },
  components: {
    Header,
    PageTitle,
    productCard,
    Footer,
  },
  created() {},
  methods: {
    setActiveSlide(slide) {
      this.activeSlide.path = require("@/assets/gallery-" + slide + ".png");
    },
    up() {
      this.qte++;
    },
    down() {
      if (this.qte > 1) this.qte--;
    },
  },
};
</script>
