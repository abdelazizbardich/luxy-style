<template>
  <div class="cards">
    <div class="container">
      <div class="row">
        <div class="offset-1 py-5 my-5 col-10">
          <div class="cards_grid">
            <div class="card_item">
              <div class="icon">
                <i class="bi bi-geo-alt-fill"></i>
              </div>
              <div class="details">
                <div class="title">livraison pour tout le Maroc</div>
                <div class="description">
                  Votre commande sera livrée à l'adresse indiquée.
                </div>
              </div>
            </div>
            <div class="card_item">
              <div class="icon">
                <i class="bi bi-credit-card-2-back-fill"></i>
              </div>
              <div class="details">
                <div class="title">paiement à la livraison</div>
                <div class="description">
                  Commandez votre produit et ne payez pas avant de l'avoir reçu.
                </div>
              </div>
            </div>
            <div class="card_item">
              <div class="icon">
                <i class="bi bi-inboxes-fill"></i>
              </div>
              <div class="details">
                <div class="title">Nouveaux produits</div>
                <div class="description">
                  Nous ajoutons de nouveaux produits chaque jour avec de bons
                  prix
                </div>
              </div>
            </div>
            <div class="card_item">
              <div class="icon">
                <i class="bi bi-mailbox2"></i>
              </div>
              <div class="details">
                <div class="title">LIVRAISON GRATUITE</div>
                <div class="description">
                  Livra ison gratuite sur toute commande supérieure à
                  <span class="text-danger">800 DH</span>
                </div>
              </div>
            </div>
            <div class="card_item">
              <div class="icon">
                <i class="bi bi-headset"></i>
              </div>
              <div class="details">
                <div class="title">SUPPORT 24/7</div>
                <div class="description">
                  Contactez-nous 24 heures sur 24, 7 jours sur 7
                </div>
              </div>
            </div>
            <div class="card_item">
              <div class="icon">
                <i class="bi bi-arrow-90deg-left"></i>
              </div>
              <div class="details">
                <div class="title">RETOUR 7 JOURS</div>
                <div class="description">
                  Renvoyez-le simplement dans les 7 jours.
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.cards {
  background-color: #f7f8fa;
  .cards_grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    position: relative;
    &::before {
      content: "";
      position: absolute;
      z-index: -1;
      background-image: url("~@/assets/cards-shape.svg");
      background-position: center center;
      background-size: contain;
      height: 300px;
      width: 300px;
      border-radius: 300px;
      left: 0%;
      top: 50%;
      transform: translate(-30%, -50%);
      z-index: -1;
      animation: cards_grid_before 35s infinite linear;
      opacity: 0.7;
    }
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
  }
}
@media screen and (max-width: 768px) {
  .cards_grid {
    grid-template-columns: repeat(1, 1fr);
  }
}
@keyframes cards_grid_before {
  form {
    transform: translate(-50%, -50%) rotate(0deg);
  }
  to {
    transform: translate(-50%, -50%) rotate(360deg);
  }
}
</style>
<script>
export default {};
</script>
