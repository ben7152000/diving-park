<template>
  <div class="container">
    <div class="row">
      <div class="col copyright">
        {{ copyright }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Copyright',
  props: {
    copyright: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped lang="scss">
.copyright {
  margin: 20px auto;
  text-align: center;
  color: #ccc;
}
</style>
