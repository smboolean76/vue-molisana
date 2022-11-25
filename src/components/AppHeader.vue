<script>
import AppLogo from "./AppLogo.vue";

export default {
  name: "AppHeader",
  components: {
    AppLogo,
  },
  data() {
    return {
      links: [
        {
          href: "#",
          label: "Home",
          active: false,
        },
        {
          href: "#",
          label: "Prodotti",
          active: true,
        },
        {
          href: "#",
          label: "Chi Siamo",
          active: false,
        },
        {
          href: "#",
          label: "Contatti",
          active: false,
        },
      ],
    };
  },
  methods: {
    changeLink(index) {
      this.links.forEach((elm, i) => {
        if (i === index) {
          elm.active = true;
        } else {
          elm.active = false;
        }
      });
    },
  },
};
</script>

<template>
  <header class="container">
    <AppLogo />
    <nav class="main-nav">
      <ul>
        <li v-for="(item, index) in links">
          <a
            :class="{ active: item.active }"
            :href="item.href"
            @click.prevent="changeLink(index)"
            >{{ item.label }}</a
          >
        </li>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
header {
  text-align: center;
  margin-bottom: 3.125rem;
  .main-nav {
    ul {
      display: flex;
      list-style: none;
      justify-content: center;

      a {
        display: inline-block;
        padding: 15px 25px;
        text-decoration: none;
        color: #000;

        &.active {
          background-color: var(--secondary-color);
        }
      }
    }
  }
}
</style>
