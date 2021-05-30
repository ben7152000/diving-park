<template>
  <div>
    <Header :logo="logo" />
    <Banner :items="items" />
    <FilterCondition
      :conditions="conditions"
      :advanced-conditions="advancedConditions"
    />
    <Footer :copyright="copyright" />
  </div>
</template>

<script>
import Header from '@/components/Header'
import Banner from '@/components/Banner'
import FilterCondition from '@/components/FilterCondition'
import Footer from '@/components/Footer'

export default {
  name: 'Index',
  components: {
    Header,
    Banner,
    FilterCondition,
    Footer,
  },
  data() {
    return {
      logo: 'Diving Park',
      copyright: 'Copyright © 2021 Made With By Diving Park',
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
    }
  },
}
</script>

<style scoped></style>
