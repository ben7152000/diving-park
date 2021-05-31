<template>
  <div>
    <Header :logo="logo" />
    <Banner class="mb-5" :items="items" />
    <div class="container my-4">
      <div class="row">
        <FilterCondition class="col-3 border rounded-0" style="height: 100%" />
        <DivingCards class="col-9" :diving-data="divingData" />
      </div>
    </div>
    <Footer :copyright="copyright" />
  </div>
</template>

<script>
import Header from '@/components/Header'
import Banner from '@/components/Banner'
import FilterCondition from '@/components/FilterCondition'
import DivingCards from '@/components/DivingCards'
import Footer from '@/components/Footer'

export default {
  name: 'Index',
  components: {
    Header,
    Banner,
    FilterCondition,
    DivingCards,
    Footer,
  },
  data() {
    return {
      // logo
      logo: 'Diving Park',

      // copyright
      copyright: 'Copyright © 2021 Made With By Diving Park',

      // banner items
      items: [
        {
          bgImgSrc: 'https://picsum.photos/1024/240/?image=10',
        },
        {
          bgImgSrc: 'https://picsum.photos/1024/240/?image=12',
        },
        {
          bgImgSrc: 'https://picsum.photos/1024/240/?image=22',
        },
      ],

      // diving cards
      divingData: [
        {
          image: 'https://picsum.photos/250/250/?image=20',
          title: '龍洞四號',
          description: '適合新手, 生物多樣, 豐富地形, 商家林立, 停車方便',
          maxDepth: '26',
          visibility: '1~8',
          location: '北部',
          degree: '簡單',
          license: ['初級潛水員證照', '進階潛水員證照', '救援潛水員證照'],
          toilet: true,
          bathroom: true,
        },
        {
          image: 'https://picsum.photos/250/250/?image=21',
          title: '潮境公園',
          description: '適合進階, 生物多樣, 豐富地形, 停車方便, 海底景觀豐富',
          maxDepth: '29',
          visibility: '1~8',
          location: '北部',
          degree: '普通',
          license: ['初級潛水員證照', '進階潛水員證照', '救援潛水員證照'],
          toilet: true,
          bathroom: true,
        },
        {
          image: 'https://picsum.photos/250/250/?image=22',
          title: '82.5k',
          description: '適合進階, 生物多樣, 停車位少, 上下岸不方便',
          maxDepth: '23',
          visibility: '1~10',
          location: '北部',
          degree: '普通',
          license: ['初級潛水員證照', '進階潛水員證照', '救援潛水員證照'],
          toilet: false,
          bathroom: false,
        },
        {
          image: 'https://picsum.photos/250/250/?image=23',
          title: '鼻頭角',
          description: '適合進階, 生物多樣, 停車位少, 上下岸不方便',
          maxDepth: '23',
          visibility: '1~10',
          location: '北部',
          degree: '普通',
          license: ['初級潛水員證照', '進階潛水員證照', '救援潛水員證照'],
          toilet: true,
          bathroom: false,
        },
        {
          image: 'https://picsum.photos/250/250/?image=24',
          title: '蝙蝠洞',
          description: '適合進階, 生物多樣, 停車位少, 上下岸不方便',
          maxDepth: '23',
          visibility: '1~10',
          location: '北部',
          degree: '普通',
          license: ['初級潛水員證照', '進階潛水員證照', '救援潛水員證照'],
          toilet: true,
          bathroom: false,
        },
      ],
    }
  },
}
</script>

<style scoped></style>
