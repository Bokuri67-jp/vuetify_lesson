<template>
  <v-container>
    <h3>職務要約</h3>
    <v-data-table :headers="resumeSummaryHeaders" :items="resumeSummary" :items-per-page="5" class="elevation-1" />
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      resumeSummaryHeaders: [
        { text: '入社年月', value: 'col1', width: '10%' },
        { text: '退社年月', value: 'col2', width: '10%' },
        { text: '在籍期間', value: 'col3', width: '10%' },
        { text: '業種', value: 'col4', width: '20%' },
        { text: '会社名', value: 'col5', width: '50%' }
      ],
      resumeSummary: [
        {
          col1: '20xx年xx月',
          col2: '20xx年xx月',
          col3: '(x年xか月)',
          col4: 'IT',
          col5: 'らぴーどあくと株式会社'
        },
        {
          col1: '20xx年xx月',
          col2: '20xx年xx月',
          col3: '(x年xか月)',
          col4: 'IT',
          col5: 'らぴーどあくと株式会社'
        },
        {
          col1: '20xx年xx月',
          col2: '20xx年xx月',
          col3: '(x年xか月)',
          col4: 'IT',
          col5: 'らぴーどあくと株式会社'
        }
      ]
    }
  }
}
</script>
