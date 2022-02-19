<template>
  <el-container>
    <el-header class="p1-header">
        <el-input v-model="input" placeholder="请输入内容"></el-input>
        <el-button type="primary">查询</el-button>
        <el-button>重置</el-button>
    </el-header>
    <el-main class="p1-main">
            <el-table
            :data="tableData"
            border
            style="width: 100%">
                <el-table-column
                    v-for="item in tableHeader"
                    :key= "item.prop"
                    :prop= "item.prop"
                    :label= "item.label">
                </el-table-column>
            </el-table>    
    </el-main>
    <el-footer>
<el-pagination
                layout="prev, pager, next"
                :total="50">
            </el-pagination>
    </el-footer>
</el-container>
</template>

<script>
export default {
    name: "Part1",
    data() {
        return {
            tableHeader: [
                {
                    prop: "Hero Image",
                    label: "Hero Image"
                },
                {
                    prop: "Hero Name",
                    label: "Hero Name"
                },
                {
                    prop: "PRO Win Rate",
                    label: "PRO Win Rate"
                },
                {
                    prop: "Pro Pick Count",
                    label: "Pro Pick Count"
                },
                {
                    prop: "Pro Ban Count",
                    label: "Pro Ban Count"
                }
            ],
            tableData: []
        }
    }
}
</script>

<style lang="scss" scoped>
    .p1-header {
        display: flex;
        justify-content: end;
        align-items: center;
        .el-input {
            width: 200px;
            margin-right: 16px;
        }
    }

    .p1-main {

    }
</style>