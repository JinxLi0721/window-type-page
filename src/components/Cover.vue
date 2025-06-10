<script setup>
import { inject } from "vue";

// 拿到 nav.vue 提供的方法
const switchTab = inject("switchTab");

const handleClick = () => {
   if (switchTab) {
      switchTab("關於");
   }
};
</script>
<template>
   <div class="cover-container d-flex justify-center flex-column">
      <div class="text-h3 text-center font-weight-bold align-self-center pb-8">雲桌面運算平台</div>
      <div class="text-subtitle-1 text-center pb-16 font-weight-medium">
         一站式 AI & 機器學習開發平台，靈活選擇開發框架與版本，輕鬆部署與運行模型。
      </div>

      <v-btn
         variant="outlined"
         color="white"
         class="font-weight-bold mx-auto mt-14"
         rounded="xl"
         size="x-large"
         append-icon="mdi-chevron-right"
         @click="handleClick"
         >開始使用
      </v-btn>
   </div>
</template>
<style scoped>
.cover-container {
   color: rgb(255, 255, 255);
   padding: 16% 12%;
   height: 100vh;
}
</style>
