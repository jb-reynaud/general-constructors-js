<template>
  <b-col lg="3" sm="6" class="mb-4 text-center">
    <b-iconstack font-scale="4">
      <b-icon stacked icon="circle-fill" variant="dark" scale="2"></b-icon>
      <b-icon stacked :icon="icon" variant="secondary"></b-icon>
    </b-iconstack>
    <h4 class="my-3 pt-4">{{ heading }}</h4>
    <p class="text-muted">{{ subheading }}</p>
  </b-col>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      required: true
    },
    heading: {
      type: String,
      required: true
    },
    subheading: {
      type: String,
      required: true
    },
  },
}
</script>
