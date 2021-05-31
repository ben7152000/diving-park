<template>
  <SwiperSide :items="items" />
</template>

<script>
import SwiperSide from './Components/SwiperSide'

export default {
  name: 'Banner',
  components: {
    SwiperSide,
  },
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style scoped lang="scss">
.banner {
  margin-bottom: 40px;
}
</style>
