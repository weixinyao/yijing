<template>
    <div class="managerlogin">
       <router-link to="{name:'about'}">
        <div class="loginimg"> 
            <img src="~@/assets/img/managerlogin.png" alt="">  
        </div>
       </router-link>
    </div>
</template>
<script>
export default {
    name: 'managerlogin'
}
</script>
<style lang="stylus" scoped>
  .managerlogin
    overflow: hidden
    width: 100%
    height: .5rem
    margin-top: .6rem
    .loginimg
      float:right
      height: .5rem
    .loginimg img
      width: 1.946667rem
      height: .413333rem
      
</style>