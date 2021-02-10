<template>
  <Layout class="login_wrapper">
    <form @submit.prevent="onSubmit" class="login">
      <h2>登录</h2>
      <label>
        账号：<input v-model="loginInfo.account" />
      </label>
      <label>
        密码：<input v-model="loginInfo.password" type="password" />
      </label>
      <div class="buttons">
        <button type="submit" class="login_btn">登录</button>
        <button type="button" class="sign_up_btn">注册</button>
      </div>
    </form>
  </Layout>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({})
export default class Login extends Vue {
  loginInfo = {
    account: '',
    password: ''
  }

  onSubmit = () => {
    console.log(this.loginInfo)
  }
}
</script>

<style lang="scss" scoped>
.login_wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  .login {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 594px;
    height: 580px;
    background: #fff;
    box-shadow: 0 3px 6px rgba(0, 0, 0, 0.08);
    border-radius: 14px;
    > h2 {
      margin: 36px 0 64px;
      font-size: 44px;
    }
    > label {
      font-size: 20px;
      &:not(:first-child) {
        margin-top: 30px;
      }
      > input {
        width: 250px;
        height: 36px;
        padding: 0 10px;
        background: #F5F5F5;
        border: 1px solid #E2E2E2;
        border-radius: 18px;
      }
    }
    > .buttons {
      margin-top: 60px;
      > button {
        width: 178px;
        height: 36px;
        font-size: 20px;
        color: #fff;
        border-radius: 18px;
      }
      > .login_btn {
        margin-right: 12px;
        background: #82B4FF;
      }
      > .sign_up_btn {
        background: #FF5858;
      }
    }
  }
}
</style>
