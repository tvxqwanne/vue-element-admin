<template>
  <div class="app-container">
     <div style='margin:0 0 20px 20px'>中蓝公寓-南楼月度用水明细</div>

    <!-- <div class="filter-container">
      <el-checkbox-group v-model="formThead">
        <el-checkbox label="apple">apple</el-checkbox>
        <el-checkbox label="banana">banana</el-checkbox>
        <el-checkbox label="orange">orange</el-checkbox>
      </el-checkbox-group>
    </div> -->

    <el-table :data="tableData" v-loading.body="listLoading" border fit highlight-current-row style="width: 100%">
      <el-table-column align="center" prop="date" label="日期" width="180">
      </el-table-column>
      <el-table-column align="center" prop="name" label="区域">
      </el-table-column>
      <el-table-column align="center" prop="address" label="用水量(立方米)">
      </el-table-column>
      <!-- <el-table-column :key='fruit' v-for='(fruit,index) in formThead' :label="fruit">
        <template scope="scope">
          {{scope.row[fruit]}}
        </template>
      </el-table-column> -->
    </el-table>

  </div>
</template>

<script>
export default {
  data() {
    return {
      tableData: [
        {
          date: '2017-09-01',
          name: '南楼',
          address: '36.84'
        },
        {
          date: '2017-09-02',
          name: '南楼',
          address: '26.71'
        },
        {
          date: '2017-09-03',
          name: '南楼',
          address: '29.58'
        },
        {
          date: '2017-09-04',
          name: '南楼',
          address: '41.48'
        },
        {
          date: '2017-09-05',
          name: '南楼',
          address: '41.72'
        },
        {
          date: '2017-09-06',
          name: '南楼',
          address: '49.14'
        },
        {
          date: '2017-09-07',
          name: '南楼',
          address: '44.50'
        },
        {
          date: '2017-09-08',
          name: '南楼',
          address: '43.74'
        },
        {
          date: '2017-09-09',
          name: '南楼',
          address: '36.16'
        },
        {
          date: '2017-09-10',
          name: '南楼',
          address: '30.36'
        },
        {
          date: '2017-09-11',
          name: '南楼',
          address: '47.38'
        },
        {
          date: '2017-09-12',
          name: '南楼',
          address: '45.62'
        },
        {
          date: '2017-09-13',
          name: '南楼',
          address: '40.25'
        },
        {
          date: '2017-09-14',
          name: '南楼',
          address: '55.24'
        },
        {
          date: '2017-09-15',
          name: '南楼',
          address: '45.13'
        },
        {
          date: '2017-09-16',
          name: '南楼',
          address: '25.93'
        },
        {
          date: '2017-09-17',
          name: '南楼',
          address: '32.77'
        },
        {
          date: '2017-09-18',
          name: '南楼',
          address: '42.47'
        },
        {
          date: '2017-09-19',
          name: '南楼',
          address: '44.38'
        },
        {
          date: '2017-09-20',
          name: '南楼',
          address: '41.01'
        },
        {
          date: '2017-09-21',
          name: '南楼',
          address: '40.49'
        },
        {
          date: '2017-09-22',
          name: '南楼',
          address: '38.77'
        },
        {
          date: '2017-09-23',
          name: '南楼',
          address: '26.67'
        },
        {
          date: '2017-09-24',
          name: '南楼',
          address: '24.80'
        },
        {
          date: '2017-09-25',
          name: '南楼',
          address: '39.11'
        },
        {
          date: '2017-09-26',
          name: '南楼',
          address: '38.66'
        },
        {
          date: '2017-09-27',
          name: '南楼',
          address: '41.01'
        },
        {
          date: '2017-09-28',
          name: '南楼',
          address: '39.32'
        }
      ]
      // ,
      // formThead: ['apple', 'banana']
    }
  }
}
</script>
