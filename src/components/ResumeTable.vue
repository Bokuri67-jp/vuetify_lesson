<template>
  <v-container>
    <v-row>
        <v-col>
          <v-card>
              <v-card-title>久保 亮太</v-card-title>
              <v-subheader>subheader</v-subheader>
              <v-card-subtitle>subtitle</v-card-subtitle>
          </v-card>
        </v-col>

        <v-col>
          <v-card>
              <v-card-title>title</v-card-title>
              <v-subheader>subheader</v-subheader>
              <v-card-subtitle>subtitle</v-card-subtitle>
          </v-card>
        </v-col>
    </v-row>
    <br>

    <v-data-table
    :headers="resumeSummaryHeaders"
    :items="resumeSummary"
    :items-per-page="5"
    class="elevation-1"
    ></v-data-table>
    <br>

    <v-data-table
    :headers="resumeHeaders"
    :items="resume"
    :items-per-page="5"
    class="elevation-1"
    ></v-data-table>
  </v-container>

</template>

<script>

export default {
  data () {
    return {
      resumeSummaryHeaders: [
        {
          text: '入社年月 - 退社年月',
          align: 'start',
          sortable: false,
          value: 'name'
        },
        { text: '在籍期間', value: 'calories' },
        { text: '業種', value: 'fat' },
        { text: '会社名', value: 'carbs' }
      ],
      resumeSummary: [
        {
          name: 'Frozen Yogurt',
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: '1%'
        },
        {
          name: 'Ice cream sandwich',
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: '1%'
        },
        {
          name: 'Eclair',
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          iron: '7%'
        },
        {
          name: 'Cupcake',
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          iron: '8%'
        }
      ],
      resumeHeaders: [
        {
          text: '入社年月 - 退社年月',
          align: 'start',
          sortable: false,
          value: 'name'
        },
        { text: '在籍期間', value: 'calories' },
        { text: '業種', value: 'fat' },
        { text: '会社名', value: 'carbs' }
      ],
      resume: [
        {
          name: 'ああああああああ',
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: '1%'
        },
        {
          name: 'Ice cream sandwich',
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: '1%'
        },
        {
          name: 'Eclair',
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          iron: '7%'
        },
        {
          name: 'Cupcake',
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          iron: '8%'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
table{
  width: 1200%;
  border: thin solid rgba(0, 0, 0, 0.12);
  th{
    border: thin solid rgba(0, 0, 0, 0.12);
  }
  td{
    border: thin solid rgba(0, 0, 0, 0.12);
  }
}
</style>
