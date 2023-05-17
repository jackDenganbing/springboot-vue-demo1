<template>
    <div style="display: flex;text-align: center" >
        <div style="width: 400px"></div>
            <el-table
                :data="tableData"
                style="width: 100%">
            <el-table-column
                    prop="type"
                    label="发明专利"
                    width="180">
            </el-table-column>
            <el-table-column
                    prop="a"
                    label="第1-3年"
                    width="180">
            </el-table-column>
            <el-table-column
                    prop="b"
                    label="第4-6年">
            </el-table-column>
                <el-table-column
                    prop="c"
                    label="第7-9年">
            </el-table-column>
            <el-table-column
                    prop="d"
                    label="第10年">
            </el-table-column>
                <el-table-column
                        prop="e"
                        label="第11-12年">
                </el-table-column>
                <el-table-column
                        prop="f"
                        label="第13-15年">
                </el-table-column>
                <el-table-column
                        prop="g"
                        label="第16-20年">
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
                    a: '900',
                    b: '1200',
                    c: '2000',
                    d: '4000',
                    e: '4000',
                    f: '6000',
                    g: '8000'
                }, {
                    type: '减缓70%',
                    a: '270',
                    b: '360',
                    c: '600',
                    d: '1200',
                    e: '4000',
                    f: '6000',
                    g: '8000'
                }, {
                    type: '减缓85%',
                    a: '135',
                    b: '180',
                    c: '300',
                    d: '600',
                    e: '4000',
                    f: '6000',
                    g: '8000'
                }, {
                    type: '滞纳第一个月',
                    a: '0',
                    b: '0',
                    c: '0',
                    d: '0',
                    e: '0',
                    f: '0',
                    g: '0'
                }, {
                    type: '滞纳第二个月',
                    a: '45',
                    b: '60',
                    c: '100',
                    d: '200',
                    e: '200',
                    f: '300',
                    g: '400'
                }, {
                    type: '滞纳第三个月',
                    a: '90',
                    b: '120',
                    c: '200',
                    d: '400',
                    e: '400',
                    f: '600',
                    g: '800'
                },{
                    type: '滞纳第四个月',
                    a: '135',
                    b: '180',
                    c: '300',
                    d: '600',
                    e: '600',
                    f: '900',
                    g: '1200'
                },{
                    type: '滞纳第五个月',
                    a: '180',
                    b: '240',
                    c: '400',
                    d: '800',
                    e: '800',
                    f: '1200',
                    g: '1600'
                },{
                    type: '滞纳第六个月',
                    a: '225',
                    b: '300',
                    c: '500',
                    d: '1000',
                    e: '1000',
                    f: '1500',
                    g: '2000'
                }
                ]
            }
        },
    }
</script>

<style scoped>

</style>