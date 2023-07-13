<script setup lang="ts">
import { RouterView } from 'vue-router'
import { zhCn } from 'element-plus/es/locale/index'
</script>

<template>
  <ElConfigProvider :locale="zhCn">
    <RouterView />
  </ElConfigProvider>
</template>

<style scoped></style>
