<template>
  <div>
    <Header :logo="logo" />
    <Banner class="mb-5" :items="items" />
    <FilterCondition />
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
    }
  },
}
</script>

<style scoped></style>
