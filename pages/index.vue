<template>
  <div>
    <Header :logo="logo" />
    <Banner :items="items" />
    <FilterCondition
      :conditions="conditions"
      :advanced-conditions="advancedConditions"
    />
    <DivingCards :diving-data="divingData" />
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

      // filter conditions
      conditions: [
        {
          collapse: '1',
          label: '地點',
          options: [{ text: '北部', value: '北部' }],
        },
        {
          collapse: '2',
          label: '難易度',
          options: [
            { text: '低', value: '低' },
            { text: '中', value: '中' },
            { text: '高', value: '高' },
          ],
        },
        {
          collapse: '3',
          label: '擁有證照',
          options: [
            { text: '初級潛水員證照 (OW)', value: '初級潛水員證照' },
            { text: '進階潛水員證照 (AOW)', value: '進階潛水員證照' },
            { text: '救援潛水員證照', value: '救援潛水員證照' },
          ],
        },
      ],

      // filter advanced conditions
      advancedConditions: [
        {
          collapse: '1',
          label: '廁所',
          options: [{ text: '有', value: '有' }],
        },
        {
          collapse: '2',
          label: '盥洗',
          options: [{ text: '有', value: '有' }],
        },
        {
          collapse: '3',
          label: '最大深度',
          options: [
            { text: '0~10 米', value: '0~10 米' },
            { text: '11~20 米', value: '11~20 米' },
            { text: '21~30 米', value: '21~30 米' },
            { text: '31~40 米', value: '31~40 米' },
          ],
        },
      ],

      // diving cards
      divingData: [
        {
          image: 'https://picsum.photos/400/400/?image=20',
          title: '龍洞四號',
          description: '適合新手, 生物多樣, 豐富地形, 商家林立, 停車方便',
          maxDepth: '26',
          visibility: '1~8',
          location: '北部',
          degree: '低',
          license: ['初級潛水員證照', '進階潛水員證照', '救援潛水員證照'],
          toilet: true,
          bathroom: true,
        },
        {
          image: 'https://picsum.photos/400/400/?image=21',
          title: '潮境公園',
          description: '適合進階, 生物多樣, 豐富地形, 停車方便, 海底景觀豐富',
          maxDepth: '29',
          visibility: '1~8',
          location: '北部',
          degree: '中',
          license: ['初級潛水員證照', '進階潛水員證照', '救援潛水員證照'],
          toilet: true,
          bathroom: true,
        },
        {
          image: 'https://picsum.photos/400/400/?image=22',
          title: '82.5k',
          description: '適合進階, 生物多樣, 停車位少, 上下岸不方便',
          maxDepth: '23',
          visibility: '1~10',
          location: '北部',
          degree: '中',
          license: ['初級潛水員證照', '進階潛水員證照', '救援潛水員證照'],
          toilet: false,
          bathroom: false,
        },
        {
          image: 'https://picsum.photos/400/400/?image=23',
          title: '鼻頭角',
          description: '適合進階, 生物多樣, 停車位少, 上下岸不方便',
          maxDepth: '23',
          visibility: '1~10',
          location: '北部',
          degree: '中',
          license: ['初級潛水員證照', '進階潛水員證照', '救援潛水員證照'],
          toilet: true,
          bathroom: false,
        },
        {
          image: 'https://picsum.photos/400/400/?image=24',
          title: '蝙蝠洞',
          description: '適合進階, 生物多樣, 停車位少, 上下岸不方便',
          maxDepth: '23',
          visibility: '1~10',
          location: '北部',
          degree: '中',
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
