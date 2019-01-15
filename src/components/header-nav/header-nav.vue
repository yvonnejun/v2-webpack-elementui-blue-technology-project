<template>
  <div class="top-wrap">
    <div class="header-nav-left">
      <div class="logo"></div>
      <div class="logo-text-wrap">
        <span class="logo-text" v-text="logoTitle"></span>
      </div>
    </div>
    <div class="header-nav-right">
      <div>
        <span>欢迎您</span>
        <el-dropdown placement="bottom-start">
          <span class="el-dropdown-link">
            {{user.userName}}<i class="el-icon-arrow-down el-icon--right"></i>
          </span>
          <!-- 通过slot来指明触发下面列表(包含在一个dropdown里面)展开的元素是上面的dropdown元素 -->
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>切换用户</el-dropdown-item>
            <el-dropdown-item>退出登录</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
        <div class="icon-bell el-icon-bell"></div>
        <div class="icon-question el-icon-question"></div>
        <!-- <div class="icon-skin"></div> -->
        <el-dropdown>
          <span class="el-dropdown-link">
            <div class="icon-skin"></div><i class="el-icon-arrow-down el-icon--right"></i>
          </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>蓝色皮肤</el-dropdown-item>
            <el-dropdown-item>红色皮肤</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </div>
    </div>
  </div>
</template>

<script>
export default { 
  name: 'header-nav',
  data () {
     /*data和return之间的地方--就是这里可以写一些内部方法供return里面的属性赋值调用*/
    return {
      logoTitle: '新农村电商后台管理系统',
      user: {
        userName: 'Lucy'
      }
    }
  },
  methods: {
    
  },
  created () {

  },
  mounted () {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
@rcolor: red;
.top-wrap {
  width: 100%;
  height: 66px;
  line-height: 66px;
  // background: #042861 url(../../assets/img/headernav/bg.png) no-repeat;
  background: #0177d5;
  background-size: 100% 100%;
  color: #fff;
  .header-nav-left {
    width: 50%;
    float: left;
    .logo {
      float: left;
      width: 103px;
      height: 66px;
      margin-left: 15px;
      font-size: 24px;
    }
    .logo:before {
      content: '';
      display: inline-block;
      width: 103px;
      height: 29px;
      background: url(../../assets/img/headernav/logo.png) no-repeat;
      vertical-align: middle;
      position: relative;
      top: -2px;
    }
    .logo-text-wrap {
      float: left;
      width: 425px;
      height: 66px;
      line-height: 66px;
      font-size: 18px;
      font-family: '微软雅黑';
      text-align: left;
      padding-left: 20px;
      .logo-text {
        padding-left: 20px;
        padding-right: 20px;
        border-left: 1px solid #fff;
        height: 24px;
  
      }
    }
  }
  .header-nav-right {
    width: 49%;
    float: right;
    .el-dropdown {
      color: #fff;
      margin-left: 25px;
    }
    .icon-bell, .icon-question,.icon-skin {
      display: inline-block;
      margin-left: 30px;
    }
    .icon-bell {
      width: 17px;
      height: 19px;
      // background: url(../../assets/img/headernav/icon-bell.jpg) no-repeat;
    }
    .icon-skin {
      width: 20px;
      height: 19px;
      background: url(../../assets/img/headernav/icon-skin.png) no-repeat;
      position: relative;
      top: 2px;
      margin-left: 10px;
    }
  }
}

</style>
