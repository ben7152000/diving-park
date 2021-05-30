<template>
  <div class="header">
    <Logo :logo="logo" />
  </div>
</template>

<script>
import Logo from './Components/Logo'
export default {
  name: 'Header',
  components: {
    Logo,
  },
  props: {
    logo: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped lang="scss"></style>
