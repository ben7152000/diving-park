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
  data() {
    return {
      logo: 'Diving Park',
    }
  },
}
</script>

<style scoped lang="scss"></style>
