<template>
  <div>
    <h4 class="title">基本選項</h4>
    <Checkbox
      v-for="(condition, index) in conditions"
      :key="index"
      :collapse="condition.collapse"
      :label="condition.label"
      :options="condition.options"
    />
    <h6 class="subtitle">高級選項</h6>
  </div>
</template>

<script>
import Checkbox from './Components/Checkbox'
export default {
  name: 'FilterCondition',
  components: {
    Checkbox,
  },
  props: {
    conditions: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style scoped lang="scss"></style>
