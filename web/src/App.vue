<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'


</script>

<template>
  <div class="full-screen">
    <RouterView />
  </div>
</template>

<style scoped>

.full-screen {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: white; /* 添加这一行，将背景色设置为白色 */
  background: url('./assets/background.png'); /* 添加这一行，设置背景图片路径 */
}
</style>