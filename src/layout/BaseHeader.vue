<template>
  <el-row class="topfix">
    <el-col :lg="1">
      <div class="collapse-btn" @click="triggerCollapse">
        <el-icon :size="20" v-show="isCollapse"><Expand /></el-icon>
        <el-icon :size="20" v-show="!isCollapse"><Fold /></el-icon>
      </div>
    </el-col>
    <el-col :lg="14">
      <el-breadcrumb class="breadcrumb" separator="/">
        <el-breadcrumb-item :to="{ path: '/' }">homepage</el-breadcrumb-item>
        <el-breadcrumb-item><a href="/">promotion management</a></el-breadcrumb-item>
        <el-breadcrumb-item>promotion list</el-breadcrumb-item>
        <el-breadcrumb-item>promotion detail</el-breadcrumb-item>
      </el-breadcrumb>
    </el-col>
    <el-col :lg="9"> </el-col>
  </el-row>
</template>
<script setup lang="ts">
import { isCollapse } from './state'

import { Fold, Expand } from '@element-plus/icons-vue'

const triggerCollapse = () => {
  isCollapse.value = !isCollapse.value
}
</script>
<style lang="scss">
.breadcrumb {
  height: 60px;
  line-height: 60px;
}
</style>
