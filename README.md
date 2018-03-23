# 微信小程序 wepyjs 第三方 点赞动画插件

### 效果：
![mark](http://oyz3pjs26.bkt.clouddn.com/blog/180323/8fBFEJD3c8.gif)






## 使用

### 安装组件
```
npm install wepy-nices --save
```

### 引入组件
```javascript
<template>
    <view catchtap="dosomethings">
        <nices :active.sync="active" :params.sync="params"></nices>
    </view>
</template>
<script>
    import wepy from 'wepy';
    import nices from 'wepy-nices';

    export default class Index extends wepy.page {
        data={
            active:false,               //必填    状态          true 已点赞 false为点赞
            params:{                    //选填    动画效果配置
                animate:'bounceIn',     //选填    点赞图标动画
                activeColor:'yellow',   //选填    已点赞图标颜色
                color:'#000',           //选填    未点赞图标颜色
                enableCancel:false      //选填    是否可取消点赞
            }
        }
        components = {
            nices
        };
        
        onLoad(){
            
        }
        
       
    }
    
</script>
```
> 注意
> 1.可用标签包住组件，触发自己的事件，改变active的值从而出发动画效果。
> 2.也可不用标签包住，组件自带切换事件，但紧切换，不返回或触发时间。
> 主要是因为考虑需要用多个时 repeat 更方便操作。所以使用1即可满足大部分需求。

---------------------------------------

###animate

动画效果引用了[animate.min.scss](https://daneden.github.io/animate.css/)

| animate        |                    |                     |                      |
| ----------------- | ------------------ | ------------------- | -------------------- |
| `bounce`          | `flash`            | `pulse`             | `rubberBand`         |
| `shake`           | `headShake`        | `swing`             | `tada`               |
| `wobble`          | `jello`            | `bounceIn`          | `bounceInDown`       |
| `bounceInLeft`    | `bounceInRight`    | `bounceInUp`        | `bounceOut`          |
| `bounceOutDown`   | `bounceOutLeft`    | `bounceOutRight`    | `bounceOutUp`        |
| `fadeIn`          | `fadeInDown`       | `fadeInDownBig`     | `fadeInLeft`         |
| `fadeInLeftBig`   | `fadeInRight`      | `fadeInRightBig`    | `fadeInUp`           |
| `fadeInUpBig`     | `fadeOut`          | `fadeOutDown`       | `fadeOutDownBig`     |
| `fadeOutLeft`     | `fadeOutLeftBig`   | `fadeOutRight`      | `fadeOutRightBig`    |
| `fadeOutUp`       | `fadeOutUpBig`     | `flipInX`           | `flipInY`            |
| `flipOutX`        | `flipOutY`         | `lightSpeedIn`      | `lightSpeedOut`      |
| `rotateIn`        | `rotateInDownLeft` | `rotateInDownRight` | `rotateInUpLeft`     |
| `rotateInUpRight` | `rotateOut`        | `rotateOutDownLeft` | `rotateOutDownRight` |
| `rotateOutUpLeft` | `rotateOutUpRight` | `hinge`             | `jackInTheBox`       |
| `rollIn`          | `rollOut`          | `zoomIn`            | `zoomInDown`         |
| `zoomInLeft`      | `zoomInRight`      | `zoomInUp`          | `zoomOut`            |
| `zoomOutDown`     | `zoomOutLeft`      | `zoomOutRight`      | `zoomOutUp`          |
| `slideInDown`     | `slideInLeft`      | `slideInRight`      | `slideInUp`          |
| `slideOutDown`    | `slideOutLeft`     | `slideOutRight`     | `slideOutUp`         |




### 更新日志
|        日期        |   版本             |       说明        |  
| ----------------- | ------------------ | -------------------| 
| 20180323        | 0.0.1           | init           | `


[本人博客：callmesoul.cn](http://callmesoul.cn)

![toast](http://nowechat.oss-cn-shenzhen.aliyuncs.com/qrcode_for_gh_b4c00b84720c_258.jpg)

