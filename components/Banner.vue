<template>
  <div class="banner">
    <SwiperSide :items="items" />
  </div>
</template>

<script>
import SwiperSide from './Components/SwiperSide'
export default {
  name: 'Banner',
  components: {
    SwiperSide,
  },
  data() {
    return {
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

<style scoped lang="scss">
.banner {
  margin-bottom: 40px;
}
</style>
