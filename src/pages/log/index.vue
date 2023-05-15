<template>
  <view class="index">
    <text>Top{{ msg }}</text>
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
import Taro from "@tarojs/taro";
import "./index.scss";

export default {
  setup() {
    const msg = ref("log page");
    Taro.usePullDownRefresh(() => {
      setTimeout(() => {
        Taro.stopPullDownRefresh();
      }, 2000);
    });
    return {
      msg,
    };
  },
};
</script>
<style>
.index {
  padding: 20px;
}
</style>
