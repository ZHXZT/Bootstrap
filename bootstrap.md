### 容器
    1.流体容器
    2.固定容器
        浏览器窗口 >= 1200 （lg 大屏pc）          width:1170
        992 < 浏览器窗口 <1200 （md 中屏pc）      width:970
        768 < 浏览器窗口 <992 （sm 平板）         width:750 (720+槽宽)
        浏览器窗口 <768 （xs 移动手机）            width:auto
    3.栅格系统
    
### 栅格源码分析
    1.流体容器和固定容器公共样式
        margin-right :auto
        margin-left :auto
        padding-left: 15px
        padding-right: 15px
    2.固定容器
        @media (min-width: @screen-sm-min) {
            width: @container-sm;
        }
        @media (min-width: @screen-md-min) {
            width: @container-md;
        }
        @media (min-width: @screen-lg-min) {
            width: @container-lg;
        }
    3.行
        margin-left: -15px
        marsin-right: -15px
    4.列
    
### 响应式工具

### 栅格盒模型设计的精妙之处
    容器两边具有15px的padding
    行 两边有-15pxmargin
    列 两边有15px的padding
    
    为了维护槽宽的规则
        列两边必须要15px的padding
    为了让列嵌套行
        行两边要有-15px的margin
    为了让容器包裹行
        容器两边要有15px的padding
