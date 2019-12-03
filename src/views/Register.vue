<template>
    <div class="container">
<van-cell-group>
  <van-field
    class="username" 
    v-model="username"
    name="username"
    required
    clearable
    label="用户名"
    right-icon="question-o"
    placeholder="请输入用户名"
    @click-right-icon="$toast('用户名不能有特殊字符')"
  />

  <van-field
    class="password"
    v-model="password"
    name="password"
    type="password"
    label="密码"
    placeholder="请输入密码"
    required
    maxlength="18"
    show-word-limit
    right-icon="question-o"
    @click-right-icon="$toast('密码长度不能超过18位')"
  />
  <van-field
    class="modifypassword"
    v-model="modifypassword"
    name="qrwdLog"
    type="password"
    label="确认密码"
    placeholder="请输入密码"
    required
    maxlength="18"
    show-word-limit
    right-icon="question-o"
    @click-right-icon="$toast('与上面密码必须一致')"
  />
</van-cell-group>
  <van-button round type="info" size="large" color="#ccc">注册</van-button>
    </div>
</template>
<script>
export default {
    name: 'register',
    data() {
        return {
            username: '',
            password: '',
            modifypassword: ''
        }
    }
}
</script>
<style lang="stylus" scoped>
  .container
    width: 100%
    height: 0
    overflow: hidden
    padding-bottom: 178%
</style>