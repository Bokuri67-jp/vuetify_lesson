<template>
  <v-container>

    <h1>職務経歴書</h1>
    <v-row>
      <v-col>
        <UserCard />
      </v-col>
      <v-col>
        <UserCard />
      </v-col>
    </v-row>
    <v-col>
      <ResumeSummary />
    </v-col>
    <v-col>
      <ResumeTable />
    </v-col>
    <v-col>
      <UserCard />
    </v-col>
  </v-container>
</template>

<script>
import UserCard from '@/components/UserCard.vue'
import ResumeSummary from '@/components/ResumeSummary.vue'
import ResumeTable from '@/components/ResumeTable'

export default {
  components: {
    UserCard,
    ResumeSummary,
    ResumeTable
  },
  mounted () {
    console.log(this.$vuetify.breakpoint.name)
  }
}
</script>
