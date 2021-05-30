<template>
  <div>
    <b-button
      :class="visible ? null : 'collapsed'"
      :aria-expanded="visible ? 'true' : 'false'"
      :aria-controls="collapse"
      @click="visible = !visible"
    >
      {{ label }}
    </b-button>
    <b-collapse :id="collapse" v-model="visible" class="mt-2">
      <b-card>
        <b-form-group v-slot="{ ariaDescribedby }">
          <b-form-checkbox-group
            v-model="selected"
            :options="options"
            :aria-describedby="ariaDescribedby"
            stacked
          />
        </b-form-group>
      </b-card>
    </b-collapse>
  </div>
</template>

<script>
export default {
  name: 'Checkbox',
  props: {
    collapse: {
      type: String,
      required: true,
    },
    label: {
      type: String,
      required: true,
    },
    options: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      selected: [],
      visible: false,
    }
  },
}
</script>

<style scoped></style>
