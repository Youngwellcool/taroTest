<template>
  <button @click="jump">日志</button>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
</template>

<script>
import { ref } from "vue";
import Taro, { onPullDownRefresh } from "@tarojs/taro";
import "./index.scss";

export default {
  setup() {
    const msg = ref("Hello world");
    const jump = () => {
      Taro.navigateTo({
        url: "pages/log/index",
      });
    };
    Taro.usePullDownRefresh(() => {
      setTimeout(() => {
        Taro.stopPullDownRefresh();
      }, 2000);
    });
    return {
      msg,
      jump,
    };
  },
};
</script>
<style>
.index {
  padding: 20px;
}
</style>
