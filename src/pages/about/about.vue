<template>
  <view class="index">
    <text>{{ msg }}</text>
    <view class="bnt" @tap="handleLink">跳转</view>
  </view>
</template>

<script setup>
import { ref } from 'vue'
import Taro from '@tarojs/taro'
import './about.scss'

const msg = ref('关于')
const handleLink = () => {
  console.log('跳转')

  Taro.navigateTo({
    url: '/pages/index/index',
  })
}
</script>
