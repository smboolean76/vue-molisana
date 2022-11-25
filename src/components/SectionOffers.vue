<script>
import AppCard from "./AppCard.vue";

export default {
  name: "SectionOffers",
  components: {
    AppCard,
  },
  data() {
    return {
      products: [
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
          titolo: "N.4 Spaghetto Quadrato Bucato",
          tipo: "lunga",
          cottura: 6,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
          titolo: "N.5 Fettuccine",
          tipo: "lunga",
          cottura: 13,
        },
      ],
    };
  },
};
</script>

<template>
  <section class="container">
    <h2>Prodotti in offerta</h2>

    <div class="products-offert">
      <AppCard
        class="offert"
        v-for="product in products"
        :img="product.src"
        :title="product.titolo"
      />
    </div>
  </section>
</template>

<style lang="scss" scoped>
h2 {
  text-align: center;
  margin-bottom: 1.25rem;
}
.products-offert {
  display: flex;
}
.offert {
  background-color: lightgreen;
  flex-grow: 1;
  border: 2px solid var(--primary-color);
}
</style>
