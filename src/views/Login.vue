<template>
    <div class="login">
        <!-- 管理员登录图标 -->
        <managerlogin></managerlogin>
        <!-- 登录图标 -->
        <logo></logo> 
        <!-- 登录注册按钮 -->
        <loginregister></loginregister> 
    </div>
</template>
<script>
import managerlogin from '@/views/logincomponents/managerlogin'
import logo from '@/views/logincomponents/logo'
import loginregister from '@/views/logincomponents/loginregister'
export default {
    name: 'login',
    components: {
       managerlogin,
       logo,
       loginregister
    }
}
</script>
<style lang="stylus" scoped>
  .login
    background: url('~@/assets/img/background.png') center center/cover  no-repeat fixed;
    width: 100%;
    height: 0;
    overflow: hidden;
    padding-bottom: 178%;
</style>