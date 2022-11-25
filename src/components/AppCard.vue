<script>
export default {
  name: "AppCard",
  props: {
    img: String,
    title: String,
  },
};
</script>

<template>
  <div class="card">
    <img :src="img" :alt="title" />
    <h3>{{ title }}</h3>
  </div>
</template>

<style lang="scss" scoped>
.card {
  padding: 0.625rem;

  h3 {
    text-align: center;
  }
  img {
    max-width: 100%;
  }
}
</style>
