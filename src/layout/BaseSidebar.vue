<template>
  <el-aside class="aside">
    <div class="title">
      <div class="logo">
        <el-icon :size="40" color="#409EFF"><ElementPlus /></el-icon>
      </div>
      <div class="title-text" v-show="!isCollapse">DRSG</div>
    </div>
    <el-scrollbar>
      <el-menu
        default-active="2"
        class="el-menu-vertical-demo"
        :collapse="isCollapse"
        mode="vertical"
        :collapse-transition="false"
        @open="handleOpen"
        @close="handleClose"
      >
        <el-sub-menu index="1">
          <template #title>
            <el-icon><location /></el-icon>
            <span>Navigator One</span>
          </template>
          <el-menu-item-group>
            <template #title><span>Group One</span></template>
            <el-menu-item index="1-1">item one</el-menu-item>
            <el-menu-item index="1-2">item two</el-menu-item>
          </el-menu-item-group>
          <el-menu-item-group title="Group Two">
            <el-menu-item index="1-3">item three</el-menu-item>
          </el-menu-item-group>
          <el-sub-menu index="1-4">
            <template #title><span>item four</span></template>
            <el-menu-item index="1-4-1">item one</el-menu-item>
            <el-menu-item index="1-4-1">item one</el-menu-item>
            <el-menu-item index="1-4-1">item one</el-menu-item>
            <el-menu-item index="1-4-1">item one</el-menu-item>
            <el-menu-item index="1-4-1">item one</el-menu-item>
            <el-menu-item index="1-4-1">item one</el-menu-item>
            <el-menu-item index="1-4-1">item one</el-menu-item>
            <el-menu-item index="1-4-1">item one</el-menu-item>
            <el-menu-item index="1-4-1">item one</el-menu-item>
            <el-menu-item index="1-4-1">item one</el-menu-item>
            <el-menu-item index="1-4-1">item one</el-menu-item>
          </el-sub-menu>
        </el-sub-menu>
        <el-menu-item index="2">
          <el-icon><icon-menu /></el-icon>
          <template #title>Navigator Two</template>
        </el-menu-item>
        <el-menu-item index="3" disabled>
          <el-icon><document /></el-icon>
          <template #title>Navigator Three</template>
        </el-menu-item>
        <el-menu-item index="4">
          <el-icon><setting /></el-icon>
          <template #title>Navigator Four</template>
        </el-menu-item>
      </el-menu>
    </el-scrollbar>
  </el-aside>
</template>

<script lang="ts" setup>
import { Location, Document, Menu as IconMenu, Setting, ElementPlus } from '@element-plus/icons-vue'
import { isCollapse } from './state'

const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
</script>
