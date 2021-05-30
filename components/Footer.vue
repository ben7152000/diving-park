<template>
  <div class="footer">
    <Copyright :copyright="copyright" />
  </div>
</template>

<script>
import Copyright from './Components/Copyright'

export default {
  name: 'Footer',
  components: {
    Copyright,
  },
  props: {
    copyright: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped lang="scss">
.footer {
  background: #444;
}
</style>
