<template>
  <div class="header_wrapper">
    <div class="container">
      <h1 class="logo"></h1>
      <nav>
        <router-link to="/">首页</router-link>
        <router-link to="/">作品集</router-link>
        <a href="https://www.yuque.com/waver-klavd" target="_blank">博客</a>
        <router-link to="/">团队资料</router-link>
        <router-link to="/">联系方式</router-link>
        <router-link to="/">留言板</router-link>
      </nav>
      <div class="user_info">
        <router-link to="/login" class="login">登录</router-link>
        <router-link to="/signUp" class="sign_up">注册</router-link>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({})
export default class Header extends Vue {
}
</script>

<style lang="scss" scoped>
$borderColor: #5a89c7;
$fontColor: #707070;
.header_wrapper {
  width: 100%;
  background: #FCFCFC;
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.08);
  > .container {
    display: flex;
    align-items: center;
    width: 1200px;
    height: 80px;
    margin: 0 auto;
    padding-right: 30px;
    > .logo {
      width: 130px;
      height: 50px;
      background: #FF4A4A;
    }
    > nav {
      display: flex;
      > a {
        margin-left: 27px;
      }
    }
    > .user_info {
      display: flex;
      width: 188px;
      height: 48px;
      margin-left: auto;
      cursor: pointer;
      > .sign_up, .login {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 50%;
        text-align: center;
        &:hover {
          text-decoration: underline;
        }
      }
      > .login {
        color: #fff;
        border-radius: 24px 0 0 24px;
        background: $borderColor;
      }
      > .sign_up {
        border: 1px solid $borderColor;
        border-radius: 0 24px 24px 0;
      }
    }
  }
}
</style>
