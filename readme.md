
# 圆形进度条、可配置、可手势滑动



# 基本使用
```
#一、引入组件
import SeekBar from '@/components/SeekBar/SeekBar.vue'

#二、注册组件
export default {
  ...
  components:{SeekBar}
  ...
}

#三、基本使用
 <SeekBar
    :width="width"
    :processVal="processVal"
    :startDeg="startDeg"
    :endDeg="endDeg"
    :max="max"
  >
  </SeekBar>`

```



# 配置项
|        参数        |     类型     |         默认值         |      描述      |
| :----------------: | :----------: | :--------------------: | :------------: |
|         id         |    String    |         Canvas         |                |
|       pageBg       |    String    |        \#FFFFFF        |  canvas背景色  |
|        lock        |   Boolean    |         false          |  滑块是否锁定  |
|       width        |    Number    |          220           |      宽度      |
|     processVal     |    Number    |           0            |     进度值     |
|        max         |    Number    |          100           |     最大值     |
|      startDeg      |    Number    |           0            | 开始角度[0-2]  |
|       endDeg       |    Number    |           1            | 结束角度[0-2]  |
|   innerLineWidth   |      B       |           1            |    内弧宽度    |
|     innerColor     | String/Array |        #e7efd9         |    内弧颜色    |
|   innerLineDash    |    Number    |  false（默认是实线）   | 内弧是否为虚线 |
|       border       |    Number    |           10           |    外弧线宽    |
|      process       |    Number    |           8            |    进度线宽    |
|     colorSatrt     | String/Array |        \#e7efd9        |    外弧颜色    |
|      colorEnd      | String/Array | ['#87AE3F', '#C4E178'] |    进度颜色    |
| isCounterClockWise |   Boolean    |         false          |  是否为逆时针  |
|     sliderSize     |    Number    |           20           |    滑块大小    |
|    sliderColor     |    String    |        #FFFFFF         |    滑块颜色    |
|  indoorCircleSize  |    Number    |           8            |  内部滑块大小  |
| indoorCircleColor  |    String    |        \#87ae3f        |  内部滑块颜色  |
|    isShowSlider    |   Boolean    |          true          |  是否显示滑块  |
|     isShowText     |   Boolean    |          true          |  是否显示文字  |


