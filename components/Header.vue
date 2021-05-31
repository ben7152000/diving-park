<template>
  <Logo :logo="logo" />
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
