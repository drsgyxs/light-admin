<template>
  <el-container>
    <BaseSidebar />
    <el-container>
      <el-header>
        <BaseHeader />
      </el-header>
      <el-main>
        <RouterView />
      </el-main>
    </el-container>
  </el-container>
</template>
<script setup lang="ts">
import BaseHeader from './BaseHeader.vue'
import BaseSidebar from './BaseSidebar.vue'
</script>
