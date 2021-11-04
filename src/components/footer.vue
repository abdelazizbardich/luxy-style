<template>
  <footer>
    <div class="footer_top">
      <div class="container">
        <div class="row">
          <div class="col-12 footer_top_row">
            <div class="newletter">
              <span>SOYEZ EN CONTACT AVEC NOUS:</span>
              <form>
                <div class="form-group">
                  <input
                    type="text"
                    placeholder="Entrer votre Email..."
                    class="form-control"
                  />
                </div>
                <div class="form-group">
                  <button type="submit" class="btn btn-dark submit">
                    REJOIGNEZ-NOUS
                  </button>
                </div>
              </form>
            </div>
            <div class="social_media">
              <a href="#"><i class="bi bi-facebook"></i></a>
              <a href="#"><i class="bi bi-twitter"></i></a>
              <a href="#"><i class="bi bi-instagram"></i></a>
              <a href="#"><i class="bi bi-pinterest"></i></a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer_middle">
      <div class="container">
        <div class="row">
          <div class="col-md-4">
            <span class="title">CATÉGORIES</span>
            <ul class="links">
              <li><a href="#">HighTech</a></li>
              <li><a href="#">Accessoires et Bijouse</a></li>
              <li><a href="#">Bauté et Santé</a></li>
              <li><a href="#">Eléctroménager/Maison</a></li>
            </ul>
          </div>
          <div class="col-md-4">
            <span class="title">À PROPOS</span>
            <p>
              Lorem ipsum dolor sit amet conse ctetur adipisicing elit, sed do
              eiusmod tempor incididunt ut labore et dolore. Lorem ipsum dolor
              sit amet conse ctetur adipisicing elit, seddo eiusmod tempor
              incididunt ut labore etdolore.
            </p>
          </div>
          <div class="col-md-4">
            <span class="title">CONTACTS</span>
            <p>
              <b>Address</b>: 2548 Broaddus Maple Court Avenue, Madisonville KY
              4783, United States of America <br /><b>Phone</b>: +777 2345 7885;
              +777 2345 7886 <br /><b>Hours</b>: 7 Days a week from 10 am to 6
              pm <br /><b>E-mail</b>: info@mydomain.com
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="footer_bottom">
      <div class="container">
        <div class="row">
          <div class="col-12 footer_bottom_flex">
            <div class="logo">
              <a href="#">
                <img src="@/assets/luxystyle-logo.svg" alt="logo" />
              </a>
            </div>
            <div class="credit">© LuxyStyle 2020. Tous droits réservés</div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
<style lang="scss" scoped>
footer {
  .footer_top {
    width: 100%;
    background-color: #04ac92;
    padding-block: 16px;
    .footer_top_row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      .newletter {
        display: flex;
        justify-content: space-between;
        align-items: center;
        font-weight: bold;
        color: #ffffff;
        form {
          margin-inline-start: 32px;
          display: flex;
          flex-direction: row;
          input {
            border-end-end-radius: 0px;
            border-start-end-radius: 0px;
            min-width: 300px;
            border: none;
            &::placeholder {
              opacity: 0.7;
              font-size: 14px;
            }
          }
          .submit {
            white-space: nowrap;
            border-start-start-radius: 0px;
            border-end-start-radius: 0px;
            border: none;
            &:hover {
              background-color: #51ffe4;
              color: black;
            }
          }
        }
      }
      .social_media {
        text-align: end;
        i {
          margin-inline: 8px;
          font-size: 20px;
          color: #ffffff;
        }
      }
    }
  }
  .footer_middle {
    padding-block: 64px;
    background-color: #f7f8fa;
    background-image: url("~@/assets/footer-bg.png");
    background-position: center center;
    background-size: contain;
    background-repeat: no-repeat;
    .title {
      font-size: 16px;
      font-weight: bold;
      text-transform: uppercase;
      margin-block-end: 16px;
      display: block;
    }
    .links {
      font-size: 14px;
      text-decoration: none;
      list-style: none;
      padding: 0;
      a {
        color: initial;
      }
      li {
        margin-block-end: 8px;
        display: block;
      }
    }
    p {
      font-size: 14px;
    }
  }
  .footer_bottom {
    .footer_bottom_flex {
      padding-block: 16px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      .logo {
        img {
          max-height: 50px;
          max-width: 130px;
        }
      }
      .credit {
        font-size: 14px;
      }
    }
  }
}
</style>
<script>
export default {};
</script>
