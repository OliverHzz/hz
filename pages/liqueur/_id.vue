<template>
  <section style="font-size: 38px;">
    <audio 
      id="musicfx" 
      loop="loop"
      autoplay="autoplay">
      <source 
        src="/music/liqueurMP3.mp3" 
        type="audio/mpeg">
    </audio>
    <div>
      <span>食品名称&nbsp;:&nbsp;</span>
      <span>烧酒话（酱酒）2019年限量版 == 茅台镇第二传奇</span>
    </div>
    <div>
      <span>配&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;料&nbsp;:&nbsp;</span>
      <span>高粱、小麦、水</span>
    </div>
    <div>
      <span>酒&nbsp;&nbsp;精&nbsp;&nbsp;度&nbsp;:&nbsp;</span>
      <span>53%vol 净含量: 500ml</span>
    </div>
    <div>
      <span>产品执行标准&nbsp;:&nbsp;</span>
      <span>GB/T26760-2011（优级）</span>
    </div>
    <div>
      <span>生产许可证号&nbsp;:&nbsp;</span>
      <span>SC1155 2038 200372</span>
    </div>
    <div>
      <span>生产日期&nbsp;:&nbsp;</span>
      <span>见包装箱</span>
    </div>
    <div>
      <span>贮存条件&nbsp;:&nbsp;</span>
      <span>在阴凉，通风，干燥处保存</span>
    </div>
    <div>
      <span>生产厂家&nbsp;:&nbsp;</span>
      <span>贵州无忧酒业（集团）有限公司</span>
    </div>
    <div>
      <span>产&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;地&nbsp;:&nbsp;</span>
      <span>贵州省仁怀市茅台镇</span>
    </div>
    <div>
      <span>全国统一零售价&nbsp;:&nbsp;</span>
      <span>3300元/瓶</span>
    </div>
    <p style="margin-top: 60px; margin-left: 24px;">过量饮酒有害健康，孕妇儿童不宜饮酒</p>
  </section>
</template>

<script>
export default {
  layout: 'liqueur',
  head() {
    return {
      title: '烧酒话'
    }
  },
  mounted() {
    document.addEventListener(
      'WeixinJSBridgeReady',
      function() {
        document.getElementById('musicfx').play()
      },
      false
    )
  }
}
</script>

<style scoped>
section {
  margin-top: 30px;
}
section > div {
  display: flex;
  line-height: 50px;
  margin-left: 24px;
}
section > div > span:nth-child(1) {
  flex-shrink: 0;
}
</style>
