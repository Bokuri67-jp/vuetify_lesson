<template>
  <v-container>
    <h3>職務経歴詳細</h3>
    <v-simple-table>
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">期間</th>
          <th class="text-left">プロジェクト内容</th>
          <th class="text-left">環境</th>
          <th class="text-left">役割 / 規模</th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in desserts"
          :key="item.name"
        >
          <td>{{ item.period }}</td>
          <td>{{ item.project }}</td>
          <td>{{ item.environment }}</td>
          <td>{{ item.role_scale }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
</v-container>
</template>

<script>
export default {
  data () {
    return {
      desserts: [
        {
          period: '20xx年xx月～20xx年xx月(x年xか月)',
          project: '中堅建設業向け基幹システム(顧客管理) の保守プロジェクト',
          environment: 'Mac, Oracle',
          role_scale: '窓口対応'
        },
        {
          period: '20xx年xx月～20xx年xx月(x年xか月)',
          project: '中堅建設業向け基幹システム(顧客管理) の保守プロジェクト',
          environment: 'Mac, Oracle',
          role_scale: '窓口対応'
        },
        {
          period: '20xx年xx月～20xx年xx月(x年xか月)',
          project: '中堅建設業向け基幹システム(顧客管理) の保守プロジェクト',
          environment: 'Mac, Oracle',
          role_scale: '窓口対応'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
table{
  width: 100%;
  .col1{ width: 15%}
  .col2{ width: 50%}
  .col3{ width: 15%}
  .col4{ width: 20%}
  th{
    border: thin solid rgba(0, 0, 0, 0.12);
    // background-color: blue;
    // color: white;
  }
  td{
    border: thin solid rgba(0, 0, 0, 0.12);
  }
}
</style>
