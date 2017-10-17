<template>
    <div class="app-container">
        <!-- <div style='margin:0 0 20px 20px'>校园南区-科学楼东进户表实时数据</div> -->
        <el-table
        :data="tableData"
        v-loading.body="listLoading" border fit highlight-current-row
        style="width: 100%">
            <el-table-column type="expand" label="水表信息">
                <template scope="props">
                    <el-form inline class="demo-table-expand">
                        <el-form-item label="水表编号">
                            <span>{{ props.row.number }}</span>
                        </el-form-item>
                        <el-form-item label="隶属部门">
                            <span>{{ props.row.department }}</span>
                        </el-form-item>
                        <el-form-item label="计量属性">
                            <span>{{ props.row.attribute }}</span>
                        </el-form-item>
                        <el-form-item label="安装地址">
                            <span>{{ props.row.location }}</span>
                        </el-form-item>
                        <el-form-item label="用水分项">
                            <span>{{ props.row.section }}</span>
                        </el-form-item>
                        <el-form-item label="用水性质">
                            <span>{{ props.row.usage }}</span>
                        </el-form-item>
                        <el-form-item label="爆管预警">
                            <span>{{ props.row.alert }}</span>
                        </el-form-item>
                        <el-form-item label="水表示数">
                            <span>{{ props.row.data }}</span>
                        </el-form-item>
                        <el-form-item label="累计示数">
                            <span>{{ props.row.sum }}</span>
                        </el-form-item>
                        <el-form-item label="原表底数">
                            <span>{{ props.row.base }}</span>
                        </el-form-item>
                    </el-form>
                </template>
            </el-table-column>
            <el-table-column label="水表名称" prop="name">
            </el-table-column>
            <el-table-column label="水表示数" prop="data">
            </el-table-column>
            <el-table-column label="通讯时间" prop="time">
            </el-table-column>
        </el-table>
    </div>
</template>

<style>
  .demo-table-expand {
    font-size: 0;
  }
  .demo-table-expand label {
    width: 180px;
    color: #99a9bf;
  }
  .demo-table-expand .el-form-item {
    margin-right: 0;
    margin-bottom: 0;
    align-self: auto;
    width: 50%;
  }
</style>

<script>
  export default {
    data() {
      return {
        tableData: [
          {
            name: '校园南区-科学楼东进户表',
            number: '0001607050022 (在线)',
            department: '北工大-电控学院',
            attribute: '该表不是总表',
            section: '实验',
            usage: '科研',
            location: '综合楼东Φ150',
            alert: '管路正常',
            data: '13321.98立方米',
            sum: '58832.98立方米',
            base: '45511.00立方米',
            time: '2017-10-16-21:03:18'
          }
        ]
      }
    }
  }
</script>