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

    <div>
      <h3>職務経歴詳細</h3>
      <table>
        <thead>
          <tr>
            <th class="col1">期間</th>
            <th class="col2">プロジェクト内容</th>
            <th class="col3">環境</th>
            <th class="col4">役割 / 規模</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>
              20xx年xx月～<br>
              20xx年xx月<br>
              (x年xか月)
            </td>
            <td>
              中堅建設業向け基幹システム(顧客管理) の保守プロジェクト<br>
              【概要】<br>
              営業活動を効果的に行うため、顧客情報を管理(更新)し、WEB上にて提供するシステムの追加開発。メンバーとして帳票の詳細設計以降を担当。
              <br>
              【担当業務】<br>
              詳細設計・プログラミング・テスト<br>
              <br>
              【ポイント】<br>
              始めての長期プロジェクトに参画する中で、お客様・協力会社様とのコミュニケーションの大切さを学んだ。相手の意見をくみ取り、場合によっては図などを用い説明する大切さを学んだ。
            </td>
            <td>
              Windows<br>
              Java<br>
              Oracle9i
            </td>
            <td>
              メンバー（PG SE）<br>
              要員数：4名<br>
              (PJ 全体：150 人)<br>
              【担当】<br>
              対会社間での連絡窓口（自社社員・協力会社社員への周知など）
            </td>
          </tr>
          <tr>
            <td>
              20xx年xx月～<br>
              20xx年xx月<br>
              (x年xか月)
            </td>
            <td>
              中堅建設業向け基幹システム(顧客管理) の保守プロジェクト<br>
              【概要】<br>
              営業活動を効果的に行うため、顧客情報を管理(更新)し、WEB上にて提供するシステムの追加開発。メンバーとして帳票の詳細設計以降を担当。
              <br>
              【担当業務】<br>
              詳細設計・プログラミング・テスト<br>
              <br>
              【ポイント】<br>
              始めての長期プロジェクトに参画する中で、お客様・協力会社様とのコミュニケーションの大切さを学んだ。相手の意見をくみ取り、場合によっては図などを用い説明する大切さを学んだ。
            </td>
            <td>
              Windows<br>
              Java<br>
              Oracle9i
            </td>
            <td>
              メンバー（PG SE）<br>
              要員数：4名<br>
              (PJ 全体：150 人)<br>
              【担当】<br>
              対会社間での連絡窓口（自社社員・協力会社社員への周知など）
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
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
