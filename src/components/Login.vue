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
      <text class="text" @click="onclick">登  录</text>
  </div>
  </div>
</template>

<script>
const modal = weex.requireModule('modal')
const navigator = weex.requireModule('navigator')
export default {
  methods: {
    onclick (event) {
      console.log('you click the button')
      var bundleUrl = weex.config.bundleUrl
      var nativeBase = bundleUrl.substring(0, bundleUrl.lastIndexOf('/') + 1)
      var platformSelect = weex.config.env.platform
      if (platformSelect === 'Web') {
        var webUrl = nativeBase + 'components/Home.html'
        navigator.push({
          url: webUrl,
          animated: 'true'
        }, event => {
          // modal.alert({message: 'you click web'})
        })
      } else if (platformSelect === 'ios') {
        var iosUrl = nativeBase + 'components/Home.js'
        navigator.push({
          url: iosUrl,
          animated: 'true'
        }, event => {
          // modal.alert({message: 'you click ios'})
        })
      } else if (platformSelect === 'android') {
        var androidUrl = nativeBase + 'components/Home.js'
        navigator.push({
          url: androidUrl,
          animated: 'true'
        }, event => {
          // modal.alert({message: 'you click android'})
        })
      }
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
  border-color: #dddddd;
  width: 300px;
}
</style>
