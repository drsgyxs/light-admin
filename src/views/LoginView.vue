<template>
  <div class="login-container">
    <div class="wrapper">
      <div class="form-box login">
        <h2>登录</h2>
        <form action="#">
          <div class="input-box">
            <span class="icon"></span>
            <input v-model="username" type="text" required />
            <label>邮箱或用户名</label>
          </div>
          <div class="input-box">
            <span class="icon"></span>
            <input v-model="password" type="password" required />
            <label>密码</label>
          </div>
          <div class="remember-forgot">
            <label>
              <input type="checkbox" />
              记住我
            </label>
            <a href="#">忘记密码？</a>
          </div>
          <button type="button" class="btn">登录</button>
        </form>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { ref, watchEffect } from 'vue'

const username = ref('')
const password = ref('')

watchEffect(() => {
  console.log(username.value, password.value)
})
</script>
<style lang="scss" scoped>
@import '@/style/login.scss';
</style>
