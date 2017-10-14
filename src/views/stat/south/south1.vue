<template>
  <div class="app-container">

    <!-- <div class="filter-container">
      <el-checkbox-group v-model="formThead">
        <el-checkbox label="apple">apple</el-checkbox>
        <el-checkbox label="banana">banana</el-checkbox>
        <el-checkbox label="orange">orange</el-checkbox>
      </el-checkbox-group>
    </div> -->

    <el-table :data="tableData" style="width: 100%">
      <el-table-column prop="date" label="日期" width="180">
      </el-table-column>
      <el-table-column prop="name" label="区域" width="180">
      </el-table-column>
      <el-table-column prop="address" label="用水量" width="180">
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
          date: '2017-05-01',
          name: '科学楼',
          address: '843.30'
        },
        {
          date: '2017-05-02',
          name: '科学楼',
          address: '1179.54'
        },
        {
          date: '2017-05-03',
          name: '科学楼',
          address: '1706.86'
        },
        {
          date: '2017-05-04',
          name: '科学楼',
          address: '1883.03'
        }
      ]
      // ,
      // formThead: ['apple', 'banana']
    }
  }
}
</script>
