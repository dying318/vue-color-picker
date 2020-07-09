支持初始化颜色、自适应容器大小方便自定义开发、返回hex、rgba/rgb两种颜色格式。

## 属性/事件列表:

| 属性/事件 | 必填 |  默认  |  功能  |
| :-----:  | :-----:  | :-----:  | :-----  |
| color  | 否 |  ''     | 初始化picker的颜色 |
| show  | 否 |   true    | 控制picker显示隐藏 |
| @pickerColor |   否   |   null   | 取色器发生取色动作触发，返回两种颜色格式：`{hex: '#ff0000', rgb: 'rgb(255, 0, 0)'}` |

![image](https://img.cdn.aliyun.dcloud.net.cn/stream/plugin_screens/f1b9de20-c194-11ea-94ae-7111464e76c8_0.png?v=1594279801)

## Demo：

```

// 这里演示在uni-modal中显示color-picker（目前组件内只有单位rpx依赖于uni-app）
<uni-modal>
    <div class="uni-mask"></div>
    <div class="uni-modal" style="padding: 20rpx;">
    <color-picker :show='true' :color="color" @pickerColor="pickerColor"></color-picker>
    <div class="actions">
        <i class="iconfont icon-del"></i>
        <i class="iconfont icon-yes"></i>
    </div>
    </div>
</uni-modal>

```

```

import colorPicker from "../../components/colorPicker";

export default {
  components: { colorPicker },
  data() {
    return {
      color: '#123456f0'
    };
  },
  methods: {
    pickerColor(color) {
      this.color = color.hex
    }
  }
};

```



