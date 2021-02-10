<template>
  <div class="card">
    <img class="show" src="" alt="">
    <div class="content">
      <div class="left">
        <span class="title">简约导航</span>
        <span class="info">使用jQuery实现的原生导航网站</span>
      </div>
      <div class="views">
        <Icon name="review" />
        <span class="count">20</span>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Icon from '@/components/Icon.vue';
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: { Icon }
})
export default class Card extends Vue {
}
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  width: 340px;
  height: 410px;
  border: 4px solid #8797B4;
  border-radius: 20px;
  > .show {
    width: 332px;
    height: 316px;
    background: #FFFFFF;
    border-radius: 20px 20px 0 0;
  }
  > .content {
    flex-grow: 1;
    display: flex;
    padding: 0 14px;
    > .left {
      flex-grow: 1;
      display: flex;
      flex-direction: column;
      > .title {
        margin: 10px 0 4px;
        font-size: 20px;
        color: #4488FF;
      }
      > .info {
        font-size: 16px;
        color: #4488FF;
      }
    }
    > .views {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      > .icon {
        width: 29px;
        height: 29px;
      }
      > .count {
        font-size: 16px;
        color: #4488FF;
      }
    }
  }
}
</style>
