<template>
  <div class="root">
    <div class="top">
        <text class="top-title">我的电站</text>
    </div>
    <div class="listParent">
    <list class="listStyle">
    <cell class="cellStyle">
    <div class="first">
      <div class="power">
        <text class="title">今日电量：</text>
        <div class="value-unit">
          <text class="value">15.06</text>
          <text class="unit"> Kwh</text>
        </div>
      </div>
      <div class="money">
        <text class="title">今日收益：</text>
        <div class="value-unit">
          <text class="value">¥56.26</text>
          <text class="unit"> K</text>
        </div>
      </div>
    </div>
    </cell>
    <cell>
    <div class="second-curve">
      <text class="title">曲线视图展位</text>
    </div>
    </cell>
    <cell>
    <div class="third-station">
      <text class="title">广州电站占位</text>
    </div>
    </cell>
    <cell>
    <div class="third-station">
      <text class="title">东莞电站占位</text>
    </div>
    </cell>
    <cell>
    <div class="third-station">
      <text class="title">深圳电站占位</text>
    </div>
    </cell>
    <cell>
    <div class="third-station">
      <text class="title">珠海电站占位</text>
    </div>
    </cell>
    </list>
    </div>
    <div>
      <text>hello</text>
    </div>
  </div>
</template>

<script>
import { WxcCell } from 'weex-ui'

export default {
  components: {
    WxcCell
  }
}
</script>

<style scoped>
.root{
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  background-color: rgb(143, 240, 123);
}
.top{
  top: 0;
  left: 0;
  height: 90px;
  background-color: rgba(80, 121, 233, 0.89);
  justify-content: center;
}
.top-title{
  font-size: 40px;
  text-align: center;
}
.listParent{
  flex: 1;
  overflow: scroll;
}
.listStyle{
  width: 800px;
}
.cellStyle{
  width: 800px;
}
.first {
  flex-direction: row;
  top: 0;
  left: 0;
  margin-top: 1px;
  height: 150px;
  background-color: #FFFFFF;
  align-items: center;
}
.second-curve{
  width: 800px;
  height: 600px;
  background-color: #FF0000;
  margin-top: 10px;
}
.third-station{
  width: 800px;
  height: 300px;
  background-color:#00FF00;
  margin-top: 10px;
}
.power {
  flex-direction: column;
  width: 300px;
  margin-left: 40px;
}
.value-unit {
  flex-direction: row;
  align-items: flex-end;
}
.money {
  flex-direction: column;
  width: 300px;
  margin-left: 40px;
}
.title {
  font-size: 25px;
  color: rgb(2, 2, 2);
}
.value {
  font-size: 70px;
  color: rgba(23, 97, 235, 0.89);
}
.unit {
  font-size: 20px;
  color: rgb(2, 2, 2);
}
</style>
