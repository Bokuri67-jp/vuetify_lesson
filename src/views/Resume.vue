<template>
  <v-container>
    <v-row>

      <h1>職務経歴書</h1>
      <v-col cols="12" sm="6" md="4">
        <ResumeTable />
      </v-col>
      <!-- <v-col>
        <ResumeTable></ResumeTable>
      </v-col> -->
      <!-- <v-col>
        <ResumeSummary />
      </v-col> -->
    </v-row>
  </v-container>
</template>

<script>
import ResumeTable from '@/components/ResumeTable'
// import ResumeSummary from '@/components/ResumeSummary.vue'

export default {
  component: {
    ResumeTable
    // ResumeSummary
  },
  mounted () {
    console.log(this.$vuetify.breakpoint.name)
  }
}
</script>
