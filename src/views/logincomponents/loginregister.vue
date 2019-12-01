<template>
    <div class="container">
        <div class="login">
            <span class="iconfont user">&#xe60e;</span>
            <input type="text" class="username"  v-validate="'required|name'" name="userName" v-model="userName" placeholder="请输入用户昵称"><br>
            <span v-show="errors.has('userName')" class="text-style"> {{ errors.first('userName') }} </span>  
        </div>
        <div class="register">
            <span class="iconfont pas">&#xe612;</span>
            <input type="password" class="password" placeholder="请输入密码" v-model="password" v-validate="'required|logpwd'" name="loginPwd">
            <span v-show="errors.has('loginPwd')" class="text-style"> {{ errors.first('loginPwd') }} </span>
        </div>
        <van-button class="log" type="primary" v-if="!isclick" color="linear-gradient(to right, #f2bdd8,#e67078)" size="large" @click="login">登录</van-button>
        <van-button class="log" v-else loading type="primary" loading-type="spinner" loading-text="登录中..." disabled size="large" color="linear-gradient(to right, #e67078, #f2bdd8)"></van-button>
        <van-button class="reg" type="primary"  color="linear-gradient(to right, #f2bdd8,#e67078 )" size="large" @click="login">注册</van-button>
    </div>
</template>
<script>
export default {
    name: 'loginregister',
    data() {
        return {
            userName: '',
            password: '',
            isclick: false
        }
    },
    methods: {
        login() {
            this.isclick = true
        }
    }
}
</script>
<style lang="stylus" scoped>
  .login
    margin-top: .4rem
    height: .94rem
    line-height: .94rem
    .user
      width:  .533333rem
      height: .94rem
      line-height: .94rem
      font-size: .666667rem
      display: inline-block
      margin-left: 1.066667rem
      color: #ff6700
    .username
      outline: none 
      border: .04rem solid #db707a
      background-color: #f9ced3
      height: .54rem
      line-height: .54rem
      margin-bottom: .266667rem
      margin-left: .4rem
      color: #666
    .text-style
      width: 100%
      height: .4rem
      display: block
      margin: 0 auto
      line-height: .4rem
      padding-left: 2rem
      color: orange
  .register
    margin-top: .6rem
    height: .94rem
    line-height: .94rem
    margin-bottom: .4rem
    .pas
      width:  .533333rem
      height: .94rem
      line-height: .94rem
      font-size: .666667rem
      display: inline-block
      margin-left: 1.066667rem
      color: #ff6700
    .password
      outline: none 
      border: .04rem solid #db707a
      background-color: #f9ced3
      height: .54rem
      line-height: .54rem
      margin-bottom: .266667rem
      margin-left: .4rem
      color: #666
    .text-style
      width: 100%
      height: .4rem
      display: block
      margin: 0 auto
      line-height: .4rem
      padding-left: 2rem
      color: orange
  .log 
    margin-top: .4rem
  .reg
    margin-top: .266667rem
</style>