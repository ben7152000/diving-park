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
  data() {
    return {
      copyright: 'Copyright © 2021 Made With By Diving Park',
    }
  },
}
</script>

<style scoped lang="scss">
.footer {
  background: #444;
}
</style>
