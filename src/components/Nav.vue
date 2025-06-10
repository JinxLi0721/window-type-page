<script setup>
import { ref, provide } from "vue";

import About from "@/components/About.vue";
import Package from "@/components/Package.vue";
import Footer from "@/components/Footer.vue";
import Cover from "@/components/Cover.vue";

const tab = ref(null);

const items = ["首頁", "關於", "套件服務", "聯絡資訊"];

// 提供一個切換 tab 的方法
const switchTab = target => {
   tab.value = target;
};

provide("switchTab", switchTab);
</script>
<template>
   <v-card :variant="text" color="#FFFFFF00">
      <v-hover v-slot="{ props: hoverProps, isHovering }">
         <v-tabs
            v-model="tab"
            align-tabs="end"
            bg-color="blue-grey-darken-4"
            v-bind="hoverProps"
            :class="['mx-auto', isHovering ? 'opacity-100' : 'opacity-50']"
         >
            <v-tab v-for="item in items" :key="item" :text="item" :value="item" color="#40C4FF"></v-tab> </v-tabs
      ></v-hover>

      <v-tabs-window v-model="tab">
         <v-tabs-window-item :key="items[0]" :value="items[0]">
            <v-card :variant="text" color="#FFFFFF00">
               <Cover></Cover>
            </v-card>
         </v-tabs-window-item>
         <v-tabs-window-item :key="items[1]" :value="items[1]">
            <v-card :variant="text" color="#FFFFFF00" class="window-height">
               <About></About>
            </v-card>
         </v-tabs-window-item>
         <v-tabs-window-item :key="items[2]" :value="items[2]">
            <v-card :variant="text" color="#FFFFFF00" class="window-height">
               <Package></Package>
            </v-card>
         </v-tabs-window-item>
         <v-tabs-window-item :key="items[3]" :value="items[3]" c>
            <v-card :variant="text" color="#FFFFFF00" lass="window-height">
               <Footer></Footer>
            </v-card>
         </v-tabs-window-item>
      </v-tabs-window>
   </v-card>
</template>
<style scoped>
.nav-container {
   z-index: 0;
   display: flex;
   justify-content: space-between;
   padding: 3px 10px;
}
.window-height {
   height: 100vh;
}
</style>
