<template>
  <b-card-img
    :src="image"
    alt="Image"
    class="rounded-0"
    style="width: 250px; height: 250px"
  />
</template>

<script>
export default {
  name: 'DivingImage',
  props: {
    image: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped></style>
