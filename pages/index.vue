<template>
  <div>
    <Header :logo="logo" />
    <Banner :items="items" />
    <FilterCondition :conditions="conditions" />
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
    }
  },
}
</script>

<style scoped></style>
