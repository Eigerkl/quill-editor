<template>
  <div class="content">
    <table>
      <thead>
        <tr>
          <th>姓名</th>
          <th>年级</th>
          <th>学校</th>
          <th>汉字</th>
          <th>因为</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="tdContent" title="1111111111111111111111111111111111111111111111111111111111111111111111111111">1111111111111111111111111111111111111111111111111111111111111111111111111111</td>
          <td class="tdContent" title="55555555555555555555555555555555555555555555555555555555555555555555555">55555555555555555555555555555555555555555555555555555555555555555555555</td>
          <td class="tdContent" title="222222222222222222222222222222222222222222222222222222222222222222222222">222222222222222222222222222222222222222222222222222222222222222222222222</td>
          <td class="tdContent" title="干干干干干干干干干干干干干干干干干干干干干">干干干干干干干干干干干干干干干干干干干干干 呱呱呱呱呱呱呱呱呱呱呱呱呱呱呱古古怪怪</td>
          <td class="tdContent" title="斤斤计较急急急急急急急急急急急急急急急斤斤计较斤斤计较急急急">斤斤计较急急急急急急急急急急急急急急急斤斤计较斤斤计较急急急</td>
        </tr>
      </tbody>
    </table>

  </div>
</template>

<script>
    export default {
        name: "pdf"
    }
</script>

<style scoped>
  .content{
    width: 900px;
    margin: 0 auto;
  }
  table{
    width: 900px;
    border-collapse:collapse;
    table-layout: fixed;
  }
  table th,table td{
    border: 1px solid #eee;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
  }
</style>
