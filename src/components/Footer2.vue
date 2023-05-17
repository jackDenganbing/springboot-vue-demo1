<template>
    <div style="display: flex;text-align: center" >
        <div style="width: 400px"></div>
            <el-table
                :data="tableData"
                style="width: 100%">
            <el-table-column
                    prop="type"
                    label="实用新型/外观设计"
                    width="180">
            </el-table-column>
            <el-table-column
                    prop="a"
                    label="第1-3年"
                    width="180">
            </el-table-column>
            <el-table-column
                    prop="b"
                    label="第4-5年">
            </el-table-column>
                <el-table-column
                    prop="c"
                    label="第6-8年">
            </el-table-column>
            <el-table-column
                    prop="d"
                    label="第9-10年">
            </el-table-column>
        </el-table>
        <div style="width: 200px"></div>
        </div>

</template>

<script>
    export default {
        name: "Footer",
        data() {
            return {
                tableData: [{
                    type: '应缴年费(标准)',
                    a: '600',
                    b: '900',
                    c: '1200',
                    d: '2000'
                }, {
                    type: '减缓70%',
                    a: '180',
                    b: '270',
                    c: '360',
                    d: '600'
                }, {
                    type: '减缓85%',
                    a: '90',
                    b: '136',
                    c: '180',
                    d: '300'
                }, {
                    type: '滞纳第一个月',
                    a: '0',
                    b: '0',
                    c: '0',
                    d: '0',
                    e: '0',
                    f: '0'
                }, {
                    type: '滞纳第二个月',
                    a: '30',
                    b: '45',
                    c: '60',
                    d: '100'
                }, {
                    type: '滞纳第三个月',
                    a: '60',
                    b: '90',
                    c: '120',
                    d: '200'
                },{
                    type: '滞纳第四个月',
                    a: '90',
                    b: '135',
                    c: '180',
                    d: '300'
                },{
                    type: '滞纳第五个月',
                    a: '120',
                    b: '180',
                    c: '240',
                    d: '400'
                },{
                    type: '滞纳第六个月',
                    a: '150',
                    b: '225',
                    c: '300',
                    d: '500'
                }
                ]
            }
        },
    }
</script>

<style scoped>

</style>