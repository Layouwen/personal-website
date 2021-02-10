<template>
  <Layout class="works_wrapper">
    <section class="works">
      <WorkItem v-for="(item, index) in [1,2,3]" :key="index" />
    </section>
  </Layout>
</template>

<script lang="ts">
import WorkItem from '@/components/Works/WorkItem.vue';
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: { WorkItem }
})
export default class Works extends Vue {
}
</script>

<style lang="scss" scoped>
@import "~@/assets/styles/helper.scss";

.works_wrapper {
  .icon {
    width: 1em;
    height: 1em;
    vertical-align: -0.15em;
    fill: currentColor;
    overflow: hidden;
  }
  > .works {
    width: 1200px;
    padding-bottom: 18px;
    margin: 0 auto;
    overflow: hidden;
  }
}
</style>
