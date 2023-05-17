<template>

    <div style="display: flex;text-align: center" >
        <div style="width: 700px"></div>
        <el-form ref="form" :model="form" label-width="80px">
            <el-form-item label="类型：">
                <el-select v-model="form.num" placeholder="请选择专利类型">
                    <el-option label="发明专利" value="1"></el-option>
                    <el-option label="实用新型/外观设计" value="2"></el-option>
                </el-select>
            </el-form-item>
            <el-form-item label="应缴年度:">
                <el-select v-model="form.year" placeholder="请选择应缴年度">
                    <el-option label="第1年" value="1"></el-option>
                    <el-option label="第2年" value="2"></el-option>
                    <el-option label="第3年" value="3"></el-option>
                    <el-option label="第4年" value="4"></el-option>
                    <el-option label="第5年" value="5"></el-option>
                    <el-option label="第6年" value="6"></el-option>
                    <el-option label="第7年" value="7"></el-option>
                    <el-option label="第8年" value="8"></el-option>
                    <el-option label="第9年" value="9"></el-option>
                    <el-option label="第10年" value="10"></el-option>
                    <el-option label="第11年" value="11"></el-option>
                    <el-option label="第12年" value="12"></el-option>
                    <el-option label="第13年" value="13"></el-option>
                    <el-option label="第14年" value="14"></el-option>
                    <el-option label="第15年" value="15"></el-option>
                    <el-option label="第16年" value="16"></el-option>
                    <el-option label="第17年" value="17"></el-option>
                    <el-option label="第18年" value="18"></el-option>
                    <el-option label="第19年" value="19"></el-option>
                    <el-option label="第20年" value="20"></el-option>
                </el-select>
            </el-form-item>
            <el-form-item label="减缓比例:">
                <el-select v-model="form.proportion" placeholder="请选择减缓比例">
                    <el-option label="无减缓" value="1"></el-option>
                    <el-option label="减缓70%" value="0.3"></el-option>
                    <el-option label="减缓85%" value="0.15"></el-option>
                </el-select>
            </el-form-item>
            <el-form-item label="滞纳时间:">
                <el-select v-model="form.late" placeholder="请选择滞纳时间">
                    <el-option label="未滞纳/滞纳1个月" value="0"></el-option>
                    <el-option label="滞纳2个月" value="0.05"></el-option>
                    <el-option label="滞纳3个月" value="0.1"></el-option>
                    <el-option label="滞纳4个月" value="0.15"></el-option>
                    <el-option label="滞纳5个月" value="0.2"></el-option>
                    <el-option label="滞纳6个月" value="0.25"></el-option>
                </el-select>
            </el-form-item>
            <el-form-item label="应缴年费:">
                <el-input type="text"
                          placeholder="0"
                          v-model="form.yearcost"
                >
                </el-input>
            </el-form-item>
            <el-form-item label="滞纳金:">
                <el-input type="text"
                          placeholder="0"
                          v-model="form.latecost"
                >
                </el-input>
            </el-form-item>
            <el-form-item label="合计:">
                <el-input type="text"
                          placeholder="0"
                          v-model="form.total"
                >
                </el-input>
            </el-form-item>
            <el-form-item>
                <el-button type="primary" @click="onSubmit()" style="alignment: center">计算</el-button>
                <el-button type="primary" @click="onClick()" style="alignment: center">专利管理</el-button>
            </el-form-item>
        </el-form>
    </div>

</template>

<script>
    import request from "../utils/request";

    export default {
        name: "Body",
        data() {
            return {
                form: {
                    num: '',
                    year: '',
                    proportion:'',
                    late:''
                }
            }
        },
        methods: {
            onSubmit() {
                 console.log('submit!');
                request.post("/api/patent/cal",this.form).then(res =>{
                   this.form = res.data;
                })
            },
            onClick() {
                // console.log('submit!');
                request.post("/api/patent/cal",this.form).then(res =>{
                    this.form = res.data;
                })
            }
        }
    }
</script>

<style scoped>

</style>