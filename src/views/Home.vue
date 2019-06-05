<template>
  <div class="home">
    <img :src="imgUrl" class="img">
    <span class="h1">{{msg}}</span>
    <iframe name="weather_inc" src="http://i.tianqi.com/index.php?c=code&id=1" width="330" height="35" frameborder="0" marginwidth="0" marginheight="0"  scrolling="no" class="tianqi"></iframe>
    
    <el-button type="text" @click="open" class="el-icon-bell">通知公告</el-button>
    
  <el-dropdown class="menu1">
  <span class="el-dropdown-link">
    测试0<i class="el-icon-arrow-down el-icon--right"></i>
  </span>
  <el-dropdown-menu slot="dropdown" class="menu3">
    <el-dropdown-item >个人资料</el-dropdown-item>
    <el-dropdown-item >修改密码</el-dropdown-item>
    <el-dropdown-item >更换皮肤</el-dropdown-item>
    <el-dropdown-item >退出</el-dropdown-item>
  </el-dropdown-menu>
</el-dropdown>
  </div>
</template>

<script>
export default {
  name: 'home',
  data() {
    return {
      imgUrl:require("../assets/logo.png"),
      msg:'智绘云平台',
    }
  },
  components: {
  },
   methods: {
      open() {
        this.$alert('欢迎来到智绘云平台', '系统公告', {
          confirmButtonText: '确定',
          callback: action => {
            this.$message({
              type: 'info',
              message: `action: ${ action }`
            });
          }
        });
      }
    }
}
</script>

<style scoped>
  .home{
    height:60px;
    width:100%;
    background:rgb(35,38,46);
    line-height:60px;
  }
  .img{
    height:40px;
    width:40px;
    margin-left:30px;
    margin-top:10px;
  }
  .h1{
    margin-left:10px;
    color:white;
    font-size:20px;
    position: absolute;
  }
  .h1:hover{
    color:rgb(105,78,58);
    cursor: pointer;
  }
  .tianqi{
    margin-left:90px;
  }
  .menu1{
    position:absolute;
    right:50px;
    top:-2px;
  }
  
  .el-icon-bell{
    color:rgb(194,194,194);
    float:right;
    margin-right:200px;
    margin-top:8px;
    font-size:15px;
  }
  .el-dropdown-link{
    color:white;
  }
  .meun3{
    width:100px;
    height:100px;
  }
</style>