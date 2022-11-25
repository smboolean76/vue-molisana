<script>
import AppCard from "./AppCard.vue";
import SectionTitle from "./SectionTitle.vue";

export default {
  name: "SectionProducts",
  components: {
    AppCard,
    SectionTitle,
  },
  data() {
    return {
      sectionTitle: "Lista Prodotti presa da Data",
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
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/6-linguine.jpg",
          titolo: "N.6 Linguine",
          tipo: "lunga",
          cottura: 12,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/7-mezze-linguine.jpg",
          titolo: "N.7 Mezze Linguine",
          tipo: "lunga",
          cottura: 11,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/11-spaghettino-quadrato.jpg",
          titolo: "n.11 Spaghettino Quadrato",
          tipo: "lunga",
          cottura: 9,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/38-mezze-maniche.jpg",
          titolo: "N.38 Mezze maniche",
          tipo: "corta",
          cottura: 12,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/44-sedani.jpg",
          titolo: "N.44 Sedani",
          tipo: "corta",
          cottura: 8,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/49-sedani.jpg",
          titolo: "N.49 Sedanini",
          tipo: "corta",
          cottura: 8,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/53-lumachine.jpg",
          titolo: "N.53 Lumachine",
          tipo: "corta",
          cottura: 12,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/55-chifferi-rigati.jpg",
          titolo: "N.55 Chifferi rigati",
          tipo: "corta",
          cottura: 12,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/58-misto-corto.jpg",
          titolo: "N.58 Misto corto",
          tipo: "corta",
          cottura: 9,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/06/84-ditale-quadrato.jpg",
          titolo: "N.84 Ditale Quadrato",
          tipo: "cortissima",
          cottura: 12,
        },
      ],
    };
  },
};
</script>

<template>
  <section class="container">
    <SectionTitle :text="sectionTitle" />
    <SectionTitle />
    <SectionTitle text="Lista Prodotti 3" />

    <div class="products">
      <!-- <div class="product" v-for="product in products">
        <img :src="product.src" :alt="product.titolo" />
        <h3>{{ product.titolo }}</h3>
      </div> -->
      <AppCard
        class="product"
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
.products {
  display: flex;
  flex-wrap: wrap;
}
.product {
  background-color: #fff;
  width: 100%;
  border: 2px solid var(--secondary-color);

  @include media-breakpoint-up(sm) {
    width: 50%;
  }

  @include media-breakpoint-up(md) {
    width: 33.33%;
  }

  @include media-breakpoint-up(lg) {
    width: 25%;
  }
}
</style>
