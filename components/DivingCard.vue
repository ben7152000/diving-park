<template>
  <b-card no-body class="overflow-hidden" style="max-width: 500px">
    <b-row no-gutters>
      <b-col md="6">
        <DivingImage :image="image" />
      </b-col>
      <b-col md="6">
        <b-card-body :title="title">
          <DivingText
            :description="description"
            :max-depth="maxDepth"
            :visibility="visibility"
            :location="location"
            :degree="degree"
            :license="license"
            :toilet="toilet"
            :bathroom="bathroom"
          />
        </b-card-body>
      </b-col>
    </b-row>
  </b-card>
</template>

<script>
import DivingImage from './Components/DivingImage'
import DivingText from './Components/DivingText'

export default {
  name: 'DivingCard',
  components: {
    DivingImage,
    DivingText,
  },
  props: {
    image: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    maxDepth: {
      type: String,
      required: true,
    },
    visibility: {
      type: String,
      required: true,
    },
    location: {
      type: String,
      required: true,
    },
    degree: {
      type: String,
      required: true,
    },
    license: {
      type: Array,
      required: true,
    },
    toilet: {
      type: Boolean,
      required: true,
    },
    bathroom: {
      type: Boolean,
      required: true,
    },
  },
}
</script>

<style scoped></style>
