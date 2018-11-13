<template>
  <!-- <text class="text">I am a new home page.</text> -->
  <wxc-tab-bar :tab-titles="tabTitles" :tab-styles="tabStyles" title-type="icon" @wxcTabBarCurrentTabSelected="wxcTabBarCurrentTabSelected">
    <div class="item-container" :style="contentStyle">
      <Main/>
    </div>
    <div class="item-container" :style="contentStyle">
      <Message/>
    </div>
    <div class="item-container" :style="contentStyle">
      <My/>
    </div>
  </wxc-tab-bar>
</template>

<script>
import Main from './Main/Main.vue'
import Message from './Message/Message.vue'
import My from './My/My.vue'
import { WxcTabBar, Utils } from 'weex-ui'
import YConfig from './yconfig'

export default {
  components: {
    WxcTabBar,
    Main,
    Message,
    My
  },
  data: () => ({
    tabTitles: YConfig.tabTitles,
    tabStyles: YConfig.tabStyles
  }),
  created () {
    const tabPageHeight = Utils.env.getPageHeight()
    const { tabStyles } = this
    this.contentStyle = { height: (tabPageHeight - tabStyles.height) + 'px' }
  },
  methods: {
    wxcTabBarCurrentTabSelected (e) {
      const index = e.page
      console.log(index)
    }
  }
}
</script>

<style scoped>
.text{
  font-size: 30px;
  color:#6666FF;
  text-align: center;
}
.item-container {
  width: 750px;
  background-color: #f2f3f4;
  align-items: center;
  justify-content: center;
}
</style>
