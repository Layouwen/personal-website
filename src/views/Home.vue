<template>
  <Layout class="home_wrapper">
    <p>学习的路上是孤独的</p>
    <p>希望我们都能坚持住这种孤独</p>
    <div class="actor_wrapper">
      <div class="line" />
      <p>梁又文</p>
    </div>
    <router-link to="works">
      <button class="start">start</button>
    </router-link>
  </Layout>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Nav from '@/components/Header.vue'

@Component({
  components: {
    Nav
  }
})
export default class Home extends Vue {

}
</script>

<style lang="scss">
.home_wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  > p {
    margin-bottom: 88px;
    font-size: 60px;
    font-weight: bold;
    color: #fff;
  }
  > .actor_wrapper {
    transform: translateX(70%);
    display: flex;
    align-items: center;
    margin-bottom: 88px;
    > .line {
      width: 100px;
      height: 6px;
      background: #fff;
      border-radius: 7px;
    }
    > p {
      margin-left: 32px;
      font-size: 60px;
      font-weight: bold;
      color: #fff;
    }
  }
  > a > .start {
    width: 450px;
    height: 100px;
    font-size: 60px;
    font-weight: bold;
    color: #fff;
    border-radius: 50px;
    background: #BDBDFF;
  }
}
</style>
