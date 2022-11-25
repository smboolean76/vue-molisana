<script>
export default {
  name: "AppLogo",
  data() {
    return {
      logo: "la-molisana-logo.png",
    };
  },
  methods: {
    getImagePath(image) {
      return new URL(image, import.meta.url).href;
    },
  },
};
</script>

<template>
  <img :src="getImagePath(`../assets/${logo}`)" alt="Logo" />
  <img :src="`/src/assets/${logo}`" alt="Logo" />
</template>

<style></style>
