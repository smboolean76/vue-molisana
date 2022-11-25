<script>
import SectionProducts from "./SectionProducts.vue";
import SectionOffers from "./SectionOffers.vue";

export default {
  name: "AppMain",
  components: {
    SectionProducts,
    SectionOffers,
  },
};
</script>

<template>
  <main>
    <SectionProducts />
    <SectionOffers />
  </main>
</template>

<style lang="scss" scoped>
// @use '../style/partials/mixins.scss' as *;

main {
  padding: 3.125rem 0;
  @include bg-img("../assets/fondo-pag-speciali.jpg");
}
</style>
