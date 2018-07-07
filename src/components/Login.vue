<template>
  <div>
  <div style="flex-direction:row; margin-bottom:40px">
      <text style="margin-right:20px">用户：</text>
      <input type="text" class="input" placeholder="请输入用户名" value="" />
  </div>
  <div style="flex-direction:row; margin-bottom:40px">
      <text style="margin-right:20px">密码：</text>
      <input type="password" class="input" placeholder="请输入密码" value="" />
  </div>
  <div class="wrapper" >
      <text class="text" @click="onclick">登录</text>
  </div>
  </div>
</template>

<script>
export default {
  methods: {
    onclick () {
      console.log('you click the button')
    }
  }
}
</script>

<style scoped>
.wrapper{
  flex-direction: column;
  justify-content: center;
  width: 470px;
  margin-top: 30px;
  margin-left: 0px;
  padding-top: 20px;
  padding-bottom: 20px;
  border-width: 2px;
  border-style: solid;
  border-color: #DDDDDD;
  background-color: #F5F5F5
}
.text{
  font-size: 30px;
  color:#666666;
  text-align: center;
}
.input{
  border-width: 1px;
  border-color: #dddddd
}
</style>
