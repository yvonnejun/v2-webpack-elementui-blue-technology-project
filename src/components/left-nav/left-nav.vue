<template>
  <div class="left-wrap">
   <el-col :span="24">
    <!-- el-menu作为父元素，背景色更可以在这里设置 background-color="#545c64"，文本颜色text-color可以在这设置，还有激活颜色active-text-color-->
    <el-menu 
      default-active="1" 
      class="el-menu-vertical-demo" 
      background-color="#0455a0"
      text-color="#fff"
      active-text-color="#ffd04b"
    >
      <el-menu-item index="1">
        <i class="el-icon-menu"></i>
        <span slot="title">区域管理</span>
      </el-menu-item>
      <el-menu-item index="2">
        <i class="el-icon-document"></i>
        <span slot="title">标签管理</span>
      </el-menu-item>
      <el-menu-item index="3">
        <i class="el-icon-share"></i>
        <span slot="title">窗口管理</span>
      </el-menu-item>
      <el-menu-item index="4">
        <i class="el-icon-tickets"></i>
        <span slot="title">事项管理</span>
      </el-menu-item>
      <el-menu-item index="5">
        <i class="el-icon-mobile-phone"></i>
        <span slot="title">人员管理</span>
      </el-menu-item>
      <el-menu-item index="6">
        <i class="el-icon-setting"></i>
        <span slot="title">基本设置</span>
      </el-menu-item>
    </el-menu>
    </el-col>
  </div>
</template>

<script>
export default { 
  name: 'left-nav',
  data () {
     /*data和return之间的地方--就是这里可以写一些内部方法供return里面的属性赋值调用*/
    return {
     
    }
  },
  methods: {
    push () {
      console.log(this.$router);
      // 对象
      // this.$router.push({path: '/login?url=' + this.$route.path}); // 记住这写法，方法前的router是带r的，属性前的route是不带r的
      this.$router.push({path: '/computed'}); // 这就跳转到了computed页面了，带参数跳转就学上面的写法即可
      // this.$route.push({path: 'computed'});
    },
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
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
.left-wrap {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  
  z-index: 2;
}
.el-menu-vertical-demo:not(.el-menu--collapse) { //这就是侧边栏菜单没有展开时的ul父元素样式
  width: 158px;
  //background-color: #0455a0; // 这是设置背景颜色的方法一，方法二是在元素标签上设置background-color="#545c64"这个属性
  //background-image: url(../../assets/img/leftnav/nav-bg.png);
  background-size: 100%;
  background-repeat: no-repeat;
  background-position-y: bottom;
  min-height: 768px;
  .el-menu-item { // 这是侧边栏li子元素的样式
    font-size: 14px;
    // color: #fff;
    padding: 0 20px;
    cursor: pointer;
    -webkit-transition: border-color .3s,background-color .3s,color .3s;
    transition: border-color .3s,background-color .3s,color .3s;
    box-sizing: border-box;
  }
}
</style>
