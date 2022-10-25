<template>
    <!-- :是v-bind的缩写，是为了动态绑定数据 -->
    <div class="m-card" :style="width? {width: width + 'px'} : {}">
        <div class="m-card-img" :style="imgHeight? {height: imgHeight + 'px'} : {}">
            <img :src="imgSrc" alt="img" />
        </div>
        <div v-if='summary' class="m-card-summary">
            {{summary}}
        </div>
        <div v-else class="m-card-summary">
            <slot></slot>
        </div>
        <slot name="footer"></slot>
    </div>
</template>
<script>
export default {
    name: "cardDemo",
    props: {
        width: {
            type: Number,
            default: 0
        },
        imgSrc: {
            type: String,
            default: ''
        },
        imgHeight: {
            type: Number,
            default: 0,
        },
        summary: {
            type: String,
            default: ''
        }
    }
}
</script>
<style lang="scss">
@import './card.scss';
.footer{
    padding:0 8px;
    font-size:12px;
    text-align:left
  }
  .level{
    color:#9199A1;
    margin-bottom: 8px;
  }
  .price{
    color:#F01414;
  }
  .footer-spring{
    display: flex;
    justify-content: space-between;
    padding: 0 8px;
    font-size: 12px;
  }
</style>
