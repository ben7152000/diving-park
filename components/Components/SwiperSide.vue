<template>
  <b-carousel
    id="carousel-fade"
    style="text-shadow: 0 0 2px #000"
    fade
    indicators
    :interval="4000"
    img-width="1024"
    img-height="240"
  >
    <b-carousel-slide
      v-for="(item, index) in items"
      :key="index"
      :img-src="item.bgImgSrc"
    ></b-carousel-slide>
  </b-carousel>
</template>

<script>
export default {
  name: 'SwiperSide',
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style scoped></style>
