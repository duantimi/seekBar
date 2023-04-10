<template>
  <view class="index">
    <SeekBar
      :width="width"
      :processVal="processVal"
      :startDeg="startDeg"
      :endDeg="endDeg"
      :max="max"
      :innerLineWidth="innerLineWidth"
      :innerLineDash="innerLineDash"
      :innerColor="innerColor"
      :border="border"
      :process="process"
      :colorSatrt="colorSatrt"
      :colorEnd="colorEnd"
      :sliderSize="sliderSize"
      :indoorCircleSize="indoorCircleSize"
      :sliderColor="sliderColor"
      :indoorCircleColor="indoorCircleColor"
      :pageBg="pageBg"
      :isShowSlider="isShowSlider"
      :lock="lock"
      :isShowText="isShowText"
      :isCounterClockWise="isCounterClockWise"
      @mouseUp="mouseUp"
      @change="change"
    >
    </SeekBar>

    <view>
      <button @click="change100">max:100</button>
      <button @click="change30">max:30</button>
      <span>是否可拖动</span><switch @change="switch2Change" />
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      width: uni.getSystemInfoSync().windowWidth, //宽度
      processVal: 20, //默认进度值
      startDeg: 8 / 9, //开始角度
      endDeg: 2 + 1 / 9, //结束角度
      max: 30, //最大值
      innerLineWidth: 5, //内弧宽度
      innerColor: '#C4E178', //内弧颜色 []/string
      innerLineDash: false, //内弧是否显示虚线，Number,默认实线
      border: 10, //圆弧宽度
      process: 8, //进度条宽度
      colorSatrt: '#e7efd9', //圆弧背景色
      colorEnd: ['#87AE3F', '#C4E178'], //进度颜色 []/string
      sliderSize: 20, //滑块大小
      indoorCircleSize: 10, //滑块内圆大小
      sliderColor: '#FFFFFF', //滑块颜色
      indoorCircleColor: '#87ae3f', //滑块内圆颜色
      pageBg: '#FFFFFF', //背景色

      isShowSlider: true, //是否显示滑块
      lock: false, //是否可以拖动,默认不锁住，不可拖动
      isShowText: true, ////是否显示文字
      isCounterClockWise: false //是否逆时针
    }
  },
  onLoad() {},
  methods: {
    mouseUp(v) {
      console.log('mouseUp', v)
    },
    change(v) {
      console.log('change', v)
    },
    change100() {
      this.max = 100
    },
    change30() {
      this.max = 30
    },
    switch2Change(e) {
      this.lock = e.detail.value
    }
  }
}
</script>

<style></style>
