<template>
  <div class="flex justify-center items-center h-screen">
    <ul class="list bg-transparent rounded-box ">

      <li class="p-4 pb-4 text-6xl  tracking-wide bg-transparent rounded-2xl text-white">
        基于人工智能的滑坡自动识别软件
      </li>


      <li class="list-row items-center">

        <img class="size-11 rounded-box flex-basis-1/2 ml-10" :src="aiicon" />

        <button class=" p-10 btn btn-primary text-3xl text-white">图片分类</button>
        <div class="flex-basis-1/2"></div>

      </li>

      <li class="list-row items-center">

        <img class="size-11 rounded-box flex-basis-1/2" :src="aiicon" />

        <button class=" p-10 btn btn-primary text-3xl text-white">图片分类</button>
        <div class="flex-basis-1/2"></div>

      </li>

    </ul>
  </div>
</template>

<script>
import { defineComponent, ref } from "vue";
import aiicon from "../assets/imgs/aislogo.svg"
export default defineComponent({
  setup() {
    return {
      aiicon
    };
  },
  components: {
  }
});
</script>

<style scoped>
/* 引入 Font Awesome 图标库 */
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css');
</style>