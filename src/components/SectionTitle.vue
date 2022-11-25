<script>
export default {
  name: "SectionTitle",
  props: {
    text: {
      type: String,
      default: "Testo di default",
    },
  },
};
</script>

<template>
  <h2>{{ text }}</h2>
</template>

<style lang="scss" scoped>
h2 {
  text-align: center;
  color: var(--primary-color);
}
</style>
