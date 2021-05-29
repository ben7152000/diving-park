<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <a href="/">{{ logo }}</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Logo',
  props: {
    logo: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped lang="scss">
a {
  font-size: 30px;
  font-weight: 700;
  color: #26bec9;

  &:hover {
    text-decoration: none;
  }
}
</style>
