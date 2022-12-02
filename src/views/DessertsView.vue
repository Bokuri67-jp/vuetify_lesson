<template>
  <Desserts />
</template>

<script>
import Desserts from '../components/Desserts'

export default {
  component: {
    Desserts
  },
  mounted () {
    console.log(this.$vuetify.breakpoint.name)
  }
}
</script>
