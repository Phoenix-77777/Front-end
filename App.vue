<template>
  <div id="app">
  <el-container>
    <el-header style="background-color: #409EFF">
    <img src="@/assets/OIP-C.jpg" alt="" style="width: 40px; position: relative; top: 10px;">
      <span style="font-size: 20px; margin-left: 15px; color: white">个人通讯录</span>

    </el-header>
  </el-container>

  <el-container>
    <el-aside style="overflow: hidden; min-height: 100vh; background-color: #F56C6C; width: 250px">
<el-menu :default-active="$route.path" router background-color="#E6A23C" text-color="#fff" active-text-color="#67C23A">
  <el-menu-item index="/">
    <i class="el-icon-s-home"></i>
    <span slot="title">系统首页</span>
  </el-menu-item>
  <el-submenu index="2">
    <template slot="title">
      <i class="el-icon-location"></i><span>用户管理</span>
    </template>
    <el-menu-item-group>
      <el-menu-item index="/admin">个人信息</el-menu-item>
      <el-menu-item index="/about">联系人信息</el-menu-item>
    </el-menu-item-group>
  </el-submenu>
  </el-menu>
    </el-aside>
    <el-main>
     <router-view/>
    </el-main>
  </el-container>
  </div>
</template>

<style>
.el-menu{
  border-right: none !important;
}
</style>
