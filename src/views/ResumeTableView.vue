<template>
  <ResumeTable />
</template>

<script>
import ResumeTable from '../components/ResumeTable'

export default {
  component: {
    ResumeTable
  },
  mounted () {
    console.log(this.$vuetify.breakpoint.name)
  }
}
</script>
