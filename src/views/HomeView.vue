<template>
  <SaleGraph />
</template>

<script>
import SaleGraph from '../components/SaleGraph'

export default {
  component: {
    SaleGraph
  },
  mounted () {
    console.log(this.$vuetify.breakpoint.name)
  }
}
</script>
