<template>
  <div id="app">
    <Header />
    <router-view />
    <Footer />
  </div>
</template>

<script lang="ts">
import Footer from '@/components/Footer.vue'
import Header from '@/components/Header.vue'
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {
    Footer,
    Header
  }
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import "~@/assets/styles/reset.scss";
</style>
