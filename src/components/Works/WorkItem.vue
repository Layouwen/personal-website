<template>
  <div class="item">
    <div class="top">
      <img class="avatar" src="" alt="">
      <div class="top_c">
        <div class="wrapper">
          <span class="name">努力了吗梁同学</span>
          <span class="time">2021年2月9日</span>
        </div>
        <div class="description">简介：React全家桶、Vue全家桶、uniapp、微信原生小程序</div>
      </div>
      <Icon @click="toggleIcon" class="icon_bottom" :name="pullDownState ? 'top' : 'bottom'" />
    </div>
    <div class="bottom" v-if="pullDownState">
      <Card v-for="(item, index) in [1,2,3]" :key="index" />
    </div>
  </div>
</template>

<script lang="ts">
import Icon from '@/components/Icon.vue';
import Card from '@/components/Works/Card.vue';
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {
    Icon,
    Card
  }
})
export default class WorkItem extends Vue {
  pullDownState = false;

  toggleIcon () {
    this.pullDownState = !this.pullDownState;
  }
}
</script>

<style lang="scss" scoped>
.item {
  width: 100%;
  padding: 0 32px;
  margin-top: 18px;
  background: #fff;
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.08);
  border-radius: 14px;
  > .top {
    display: flex;
    align-items: center;
    height: 122px;
    > .avatar {
      width: 66px;
      height: 66px;
      background: #C57070;
      border-radius: 50%;
      overflow: hidden;
    }
    > .top_c {
      flex-grow: 1;
      padding-left: 21px;
      color: #4488FF;
      > .wrapper {
        color: inherit;
        > .name {
          margin-right: 20px;
          font-size: 30px;
          font-weight: bold;
          color: inherit;
        }
        > .time {
          font-size: 20px;
          color: inherit;
        }
      }
      > .description {
        font-size: 20px;
        color: inherit;
      }
    }
    > .icon_bottom {
      height: 67px;
      width: 67px;
    }
  }
  > .bottom {
    display: flex;
    justify-content: space-between;
    padding-bottom: 63px;
  }
}
</style>
