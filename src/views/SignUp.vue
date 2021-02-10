<template>
  <Layout class="sign_up_wrapper">
    <form @submit.prevent="onSubmit" class="sign_up">
      <h2>注册</h2>
      <label>
        账号：<input v-model="signUpInfo.account" />
      </label>
      <label>
        密码：<input v-model="signUpInfo.password" type="password" />
      </label>
      <label>
        确认密码：<input v-model="signUpInfo.confirmPassword" type="password" />
      </label>
      <div class="buttons">
        <button type="submit" class="sign_up_btn">注册</button>
      </div>
    </form>
  </Layout>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({})
export default class Login extends Vue {
  signUpInfo = {
    account: '',
    password: '',
    confirmPassword: ''
  }

  onSubmit = () => {
    console.log(this.signUpInfo)
  }
}
</script>

<style lang="scss" scoped>
.sign_up_wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  .sign_up {
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
      display: flex;
      justify-content: flex-end;
      width: 350px;
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
      > .sign_up_btn {
        width: 236px;
        height: 36px;
        font-size: 20px;
        color: #fff;
        background: #82B4FF;
        border-radius: 18px;
      }
    }
  }
}
</style>
