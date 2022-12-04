<template>
  <div>
    <table>
      <div v-for="tr in rows" :key="tr.index">
        <tr>
          <div v-for="cell in tr.table_cells" :key="cell.index">
            <td>ddd
              <p>sss</p>
            </td>
          </div>
        </tr>
      </div>
    </table>
  </div>
</template>

<script>
export default {
  data () {
    return {
      rows: [
        {
          table_cells: [
            { name: 'a' }
          ]
        },
        {
          table_cells: [
            {},
            {},
            {}
          ]
        },
        {
          table_cells: [
            {},
            {},
            {}
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
table{
  width: 40%;
  td{
    border: thin solid rgba(0, 0, 0, 0.12);
  }
}
</style>
