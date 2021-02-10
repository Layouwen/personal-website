<template>
  <div id="app">
    <Nav />
    <router-view />
    <Footer />
  </div>
</template>

<script lang="ts">
import Footer from '@/components/Footer.vue'
import Nav from '@/components/Header.vue'
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {
    Footer,
    Nav
  }
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import "~@/assets/styles/reset.scss";
</style>
