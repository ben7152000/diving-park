<template>
  <b-card-text>
    {{ description }}
    <br />
    最大深度 : {{ maxDepth }}
    <br />
    地點 : {{ location }}
    <br />
    廁所 :
    <span v-if="toilet">有</span>
    <span v-else>無</span>
    盥洗 :
    <span v-if="bathroom">有</span>
    <span v-else>無</span>
  </b-card-text>
</template>

<script>
export default {
  name: 'DivingText',
  props: {
    description: {
      type: String,
      required: true,
    },
    maxDepth: {
      type: String,
      required: true,
    },
    visibility: {
      type: String,
      required: true,
    },
    location: {
      type: String,
      required: true,
    },
    degree: {
      type: String,
      required: true,
    },
    license: {
      type: Array,
      required: true,
    },
    toilet: {
      type: Boolean,
      required: true,
    },
    bathroom: {
      type: Boolean,
      required: true,
    },
  },
}
</script>

<style scoped></style>
