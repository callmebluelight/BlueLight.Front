<script setup>
import TopList from './components/TopList.vue'
import ArticleList from './components/ArticleList.vue';
</script>

<template>
  <el-row>
    <el-col :span="24">
      <div class="grid-content bg-purple-dark">
        <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
          <el-menu-item index="1"><router-link to="/">首页</router-link></el-menu-item>          
          <el-menu-item index="2"><router-link to="/detail/12222111">明细</router-link></el-menu-item> 
          <el-menu-item index="3"> <router-link to="/about">关于</router-link></el-menu-item>
        </el-menu>
      </div>
    </el-col>
  </el-row>
  <el-row :gutter="20">
    <el-col :span="4"> <el-menu default-active="2" class="el-menu-vertical-demo" @open="handleOpen" @close="handleClose">

        <el-menu-item index="2">
          <i class="el-icon-menu"></i>
          <span slot="title">导航二</span>
        </el-menu-item>
        <el-menu-item index="3" disabled>
          <i class="el-icon-document"></i>
          <span slot="title">导航三</span>
        </el-menu-item>
        <el-menu-item index="4">
          <i class="el-icon-setting"></i>
          <span slot="title">导航四</span>
        </el-menu-item>
      </el-menu></el-col>
    <el-col :span="20">
    
      <router-view>
      </router-view>
    </el-col>

  </el-row>
  <el-row>
    <el-col :span="24">
      <div class="grid-content bg-purple-dark"></div>
    </el-col>
  </el-row>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

.el-row {
  margin-bottom: 20px;

}

.el-col {
  border-radius: 4px;
}

.bg-purple-dark {
  background: #2a6ac4;
}

.bg-purple {
  background: #d41212;
}

.bg-purple-light {
  background: #e5e9f2;
}

.grid-content {
  border-radius: 4px;
  min-height: 36px;
}

.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
</style>