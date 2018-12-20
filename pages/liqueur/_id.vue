<template>
  <section style="font-size: 38px;">
    <audio 
      id="musicfx" 
      loop="loop"
      autoplay="autoplay">
      <source 
        :src="music"
        type="audio/mpeg">
    </audio>
    <div 
      v-for="(info, index) in infos" 
      :key="index">
      <span>{{ info.title }}</span>
      <span>{{ info.text }}</span>
    </div>
    <p style="margin-top: 60px; margin-left: 24px;">过量饮酒有害健康，孕妇儿童不宜饮酒</p>
    <section class="images">
      <img
        v-for="(image, index) in images"
        :key="index"
        :src="image">
    </section>
  </section>
</template>

<script>
export default {
  layout: 'liqueur',
  head() {
    let title = ''
    if (this.$route.params.id === '1') {
      title = '烧酒话'
    } else if (this.$route.params.id === '2') {
      title = '烧酒话'
    } else if (this.$route.params.id === '3') {
      title = '吴氏宗亲酒'
    }
    return {
      title: title
    }
  },
  data() {
    return {
      infos: [],
      music: '',
      images: []
    }
  },
  created() {
    if (this.$route.params.id === '1') {
      this.infos = [
        {
          title: '食品名称 : ',
          text: '烧酒话（酱酒）2019年限量版 == 茅台镇第二传奇'
        },
        { title: '配 料 : ', text: '高粱、小麦、水' },
        {
          title: '酒 精 度 : ',
          text: '53%vol'
        },
        {
          title: '净含量 : ',
          text: '500ml'
        },
        {
          title: '产品执行标准 : ',
          text: 'GB/T26760-2011（优级）'
        },
        {
          title: '生产许可证号 : ',
          text: 'SC1155 2038 200372'
        },
        {
          title: '生产日期 : ',
          text: '见包装箱'
        },
        {
          title: '贮存条件 : ',
          text: '在阴凉，通风，干燥处保存'
        },
        {
          title: '生产厂家 : ',
          text: '贵州无忧酒业（集团）有限公司'
        },
        {
          title: '产 地 : ',
          text: '贵州省仁怀市茅台镇'
        },
        {
          title: '全国统一零售价 : ',
          text: '3300元/瓶'
        }
      ]
      this.music = '/music/liqueurMP3.mp3'
      this.images = [
        '/images/image01.jpg',
        '/images/image02.jpg',
        '/images/image03.jpg',
        '/images/image04.jpg',
        '/images/image05.jpg',
        '/images/image06.jpg'
      ]
    } else if (this.$route.params.id === '2') {
      this.infos = [
        {
          title: '食品名称 : ',
          text: '烧酒话（酱酒）'
        },
        { title: '配 料 : ', text: '高粱、小麦、水' },
        {
          title: '酒 精 度 : ',
          text: '53%vol'
        },
        {
          title: '净含量 : ',
          text: '500ml'
        },
        {
          title: '产品执行标准 : ',
          text: 'GB/T26760-2011（优级）'
        },
        {
          title: '生产许可证号 : ',
          text: 'SC1155 2038 200372'
        },
        {
          title: '生产日期 : ',
          text: '见包装箱'
        },
        {
          title: '贮存条件 : ',
          text: '在阴凉，通风，干燥处保存'
        },
        {
          title: '生产厂家 : ',
          text: '贵州无忧酒业（集团）有限公司'
        },
        {
          title: '产 地 : ',
          text: '贵州省仁怀市茅台镇'
        },
        {
          title: '全国统一零售价 : ',
          text: '1680元/瓶'
        }
      ]
      this.music = '/music/liqueurMP3.mp3'
      this.images = [
        '/images/image01.jpg',
        '/images/image02.jpg',
        '/images/image03.jpg',
        '/images/image04.jpg',
        '/images/image05.jpg',
        '/images/image06.jpg'
      ]
    } else if (this.$route.params.id === '3') {
      this.infos = [
        {
          title: '食品名称 : ',
          text: '吴氏宗亲酒（酱香型）'
        },
        { title: '配 料 : ', text: '高粱、小麦、水' },
        {
          title: '酒 精 度 : ',
          text: '53%vol'
        },
        {
          title: '净含量 : ',
          text: '500ml'
        },
        {
          title: '生产厂家 : ',
          text: '贵州茅台镇赛台酒业集团'
        },
        {
          title: '产 地 : ',
          text: '贵州省仁怀市茅台镇'
        },
        {
          title: '全国统一零售价 : ',
          text: '598元/瓶'
        }
      ]
      this.music = '/music/aipincaihuiying.mp3'
      this.images = [
        '/images/image01.jpg',
        '/images/image02.jpg',
        '/images/image03.jpg',
        '/images/image04.jpg',
        '/images/image05.jpg'
      ]
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
section > div > span:nth-child(2) {
  margin-left: 5px;
}
.images {
  width: 100%;
}
.images img {
  display: block;
  width: 100%;
}
</style>
