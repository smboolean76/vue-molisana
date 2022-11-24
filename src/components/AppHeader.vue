<script>
import AppLogo from './AppLogo.vue';

export default {
  name: 'AppHeader',
  components: {
    AppLogo
  },
  data() {
    return {
        links: [
            'Home',
            'Prodotti',
            'Chi Siamo',
            'Contatti'
        ]
    }
  }
}
</script>

<template>
    <header class="container">
        <AppLogo/>
        <nav class="main-nav">
            <ul>
                <li v-for="link in links"><a href="">{{link}}</a></li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
header {
    text-align: center;
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
