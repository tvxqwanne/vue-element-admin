<template>
  <div class="app-container">
    <div style='margin:0 0 20px 20px' align='center'>校园南区-科学楼东进户表实时数据</div>
    <east-table></east-table>

    <div style='margin:30px 0 20px 20px align:center' align='center'>24h用水状况图</div>
    <east-chart></east-chart>
  </div>
</template>

<script>
import eastTable from './eastTable'
import eastChart from './eastChart'

export default {
  components: { eastTable, eastChart }
}
</script>

