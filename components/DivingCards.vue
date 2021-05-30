<template>
  <div>
    <DivingCard
      v-for="(data, index) in divingData"
      :key="index"
      :image="data.image"
      :title="data.title"
      :description="data.description"
      :max-depth="data.maxDepth"
      :visibility="data.visibility"
      :location="data.location"
      :degree="data.degree"
      :license="data.license"
      :toilet="data.toilet"
      :bathroom="data.bathroom"
    />
  </div>
</template>

<script>
import DivingCard from './DivingCard'

export default {
  name: 'DivingCards',
  components: {
    DivingCard,
  },
  props: {
    divingData: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style scoped></style>
