<template>
<div>
<div class="top">

</div>
   
    <el-form :inline="true" :model="formInline" class="demo-form-inline">
    <el-select v-model="formInline.region" placeholder="2019">
    <el-option label="2018" value="shanghai"></el-option>
    <el-option label="2019" value="beijing"></el-option>
 </el-select>
  <el-form-item >
    <el-input v-model="formInline.user" placeholder="请输入关键字"></el-input>
  </el-form-item>
  <el-form-item >
  </el-form-item>
  <el-form-item>
    <el-button type="primary" @click="onSubmit">查询</el-button>
    <router-link to="/Xinjian"><el-button type="primary" @click="onSubmit" class="nav1">新建项目</el-button></router-link>
    <el-button type="primary" @click="onSubmit" class="nav2">修改</el-button>
    <el-button type="primary" @click="onSubmit" class="nav3">删除</el-button>
  </el-form-item>
  </el-form>
</div>
</template>

<script>
export default {
     data() {
      return {
        formInline: {
          user: '',
          region: ''
        }
      }
    },
    methods: {
      onSubmit() {
        console.log('submit!');
      }
    }
}
</script>

<style scoped>
.top{
    height:40px;
    border-bottom:1px solid rgb(226,226,226)
}
.demo-form-inline{
    margin-left:40px;
}
.nav1{
    background:rgb(73,176,252);
    margin-left:10px;
}
.nav2{
    background:rgb(255,184,1);
    margin-left:10px;
}
.nav3{
    background:rgb(255,88,35)
}
</style>