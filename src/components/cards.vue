<template>
  <div class="cards">
    <div class="container">
      <div class="row justify-content-center">
        <div class="py-3 py-md-5 my-5 my-md-5 col-md-10">
          <div class="cards_grid">
            <CardItem
              icon="bi bi-geo-alt-fill"
              title="livraison pour tout le Maroc"
              description="Votre commande sera livrée à l'adresse indiquée."
            />
            <CardItem
              icon="bi bi-credit-card-2-back-fill"
              title="paiement à la livraison"
              description="Commandez votre produit et ne payez pas avant de l'avoir reçu."
            />
            <CardItem
              icon="bi bi-inboxes-fill"
              title="Nouveaux produits"
              description="Nous ajoutons de nouveaux produits chaque jour avec de bons
                  prix"
            />
            <CardItem
              icon="bi bi-mailbox2"
              title="LIVRAISON GRATUITE"
              description="Livraison gratuite sur toute commande supérieure à
                  <span class='text-danger'>800 DH</span>"
            />
            <CardItem
              icon="bi bi-headset"
              title="SUPPORT 24/7"
              description="Contactez-nous 24 heures sur 24, 7 jours sur 7"
            />
            <CardItem
              icon="bi bi-arrow-90deg-left"
              title="RETOUR 7 JOURS"
              description="Renvoyez-le simplement dans les 7 jours."
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.cards {
  background-color: #f7f8fa;
  position: relative;
  z-index: -1;
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
  }
}
@media screen and (max-width: 768px) {
  .cards {
    overflow: hidden;
    .cards_grid {
      grid-template-columns: repeat(2, 1fr);
      &::before {
        height: 500px;
        width: 500px;
        border-radius: 500px;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        opacity: 1;
      }
    }
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
import CardItem from "@/components/subcomponents/card-item.vue";
export default {
  components: {
    CardItem,
  },
};
</script>
