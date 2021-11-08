<template>
  <div class="contact">
    <Header />
    <PageTitle :title="'Contact'" />
    <div class="container">
      <div class="row">
        <div class="col-12 col-md-8 m-auto">
          <div class="form">
            <form>
              <div class="form-group">
                <label for="name">Nom complet:</label>
                <input
                  id="name"
                  type="text"
                  placeholder="Tapez votre nom et prénom..."
                  class="form-control"
                />
              </div>
              <div class="form-group">
                <label for="email">Adresse email:</label>
                <input
                  id="email"
                  type="text"
                  placeholder="Votre adresse email..."
                  class="form-control"
                />
              </div>
              <div class="form-group">
                <label for="subject">Sujet:</label>
                <input
                  id="subject"
                  type="text"
                  placeholder="Le sujet de votre message..."
                  class="form-control"
                />
              </div>
              <div class="form-group">
                <label for="message">Message:</label>
                <textarea
                  placeholder="Tapez votre message..."
                  id="message"
                  cols="30"
                  rows="10"
                  class="form-control"
                ></textarea>
              </div>
              <span class="helper"
                >les champs avec le signe (<span class="text-danger">*</span>)
                sont obligatoires</span
              >
              <div class="form-group">
                <button type="submit" class="btn btn-primary">Envoyez</button>
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
.contact {
  .form {
    min-height: 70vh;
    padding: 64px;
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
}
@media screen and (max-width: 768px) {
  .contact {
    .form {
      padding: 16px;
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
