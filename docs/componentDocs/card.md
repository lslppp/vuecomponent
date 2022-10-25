# Card
卡片组件

## 示例
<br/>
<cardDemo width=300 imgSrc="/4.jpg" imgHeight=150 summary="冬日观雪，滑雪，露营，夏令营">
      <template v-slot:footer>
        <div class="footer-spring">
          <div class="level">夏令营报名人数:298</div>
          <div class="price">10340收藏</div>
        </div>
      </template>
</cardDemo>

## 代码
```html
<cardDemo width=300 imgSrc="/4.jpg" imgHeight=150 summary="冬日观雪，滑雪，露营，夏令营">
      <template v-slot:footer>
        <div class="footer-spring">
          <div class="level">夏令营报名人数:298</div>
          <div class="price">10340收藏</div>
        </div>
      </template>
</cardDemo>
```

### Attributes
| 参数  | 说明   | 类型 | 是否必要 | 默认值 |
| ------| ----- | ---- | ------- | ------ |
| width | 卡片的宽度 | Number| false | - |
| imgSrc| 图片的资源地址 | String | true | - |
| imgHeight | 图片高度 | Number | false | - |
|summary| 卡片概要 | String/Slot | false | - |
| footer| 卡片底部 | Slot | false | - |