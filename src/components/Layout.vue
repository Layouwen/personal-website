<template>
  <main class="layout">
    <slot />
  </main>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({})
export default class Layout extends Vue {
}
</script>

<style lang="scss" scoped>
.layout {
  min-height: calc(100vh - 80px - 100px);
  background: #C3EDFE;
}
</style>
