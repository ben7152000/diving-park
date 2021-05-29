<template>
  <div>
    <Header />
    <Banner />
    <FilterCondition />
    <Footer />
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
}
</script>

<style scoped></style>
