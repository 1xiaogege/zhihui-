<template>
<div class="menu">

    <el-menu
      default-active="2"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-fonticon-test"></i>
          <span>项目和人员管理</span>
        </template>
          <router-link to="/H"><el-menu-item index="2-1">项目管理</el-menu-item></router-link>
          <el-menu-item index="2-2">人员管理</el-menu-item>
          <el-menu-item index="2-3">编录总模板</el-menu-item>
      </el-submenu>
      <el-submenu index="2">
        <template slot="title">
          <i class="el-icon-fontziliao"></i>
          <span>项目资料管理</span>
        </template>
        <el-menu-item-group >
          <el-menu-item index="1-1">项目地图</el-menu-item>
          <el-menu-item index="1-2">项目文件管理</el-menu-item>
          <el-menu-item index="1-2">钻孔布置一览表</el-menu-item>
          <el-menu-item index="1-2">钻孔编录信息</el-menu-item>
          <el-menu-item index="1-2">调绘点信息</el-menu-item>
          <el-menu-item index="1-2">调绘图层</el-menu-item>
        </el-menu-item-group>
      </el-submenu>
      <el-submenu index="3">
        <template slot="title">
          <i class="el-icon-fonticon-test"></i>
          <span>考勤管理</span>
        </template>
        <el-menu-item-group >
          <el-menu-item index="1-1">工作量统计</el-menu-item>
          <el-menu-item index="1-2">人员考勤</el-menu-item>
        </el-menu-item-group>
      </el-submenu>
      <el-submenu index="4">
        <template slot="title">
          <i class="el-icon-fontjuecezhongxin"></i>
          <span>决策管理</span>
        </template>
        <el-menu-item-group >
          <el-menu-item index="1-1">热力图</el-menu-item>
        </el-menu-item-group>
      </el-submenu>
      <el-submenu index="5">
        <template slot="title">
          <i class="el-icon-fontyidongshebei"></i>
          <span>移动设备管理</span>
        </template>
        <el-menu-item-group >
          <el-menu-item index="1-1">移动设备</el-menu-item>
        </el-menu-item-group>
      </el-submenu>
      <el-submenu index="6">
        <template slot="title">
          <i class="el-icon-fonticon-test1"></i>
          <span>北斗实时通讯</span>
        </template>
      </el-submenu>
    </el-menu>

</div>
</template>

<script>
 export default {
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>


<style scoped>
.el-menu-vertical-demo{
  width:200px;
}
  .menu{
    width:200px;
    background:rgb(84,92,100);
    position: absolute;
    top:60px;
    bottom:0;
  }
</style>