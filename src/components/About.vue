<script setup>
import aboutFeature from "../stores/aboutFeature.json";
</script>
<template>
   <div class="container d-flex justify-center flex-column">
      <div class="text-h4 text-center font-weight-bold align-self-center py-3">核心特色</div>
      <v-divider class="border-opacity-75 ma-auto" :thickness="4" width="60%"></v-divider>
      <div class="text-subtitle-1 text-center py-3 font-weight-medium">
         只需透過網頁桌面操作，完成所有開發或分析相關工作，提供絕佳體驗
      </div>
      <v-row class="pt-10">
         <v-col cols="12" md="3" v-for="card in aboutFeature">
            <v-card :variant="flat" class="mx-auto hover-scale" color="blue-grey-darken-4" min-height="390">
               <v-img height="150px" :src="`./icons/${card.img}`" cover></v-img>

               <v-card-item>
                  <v-card-title class="text-h5 font-weight-bold">{{ card.title }}</v-card-title>

                  <v-card-subtitle>{{ card.subtitle }}</v-card-subtitle>
               </v-card-item>

               <v-card-text class="text-button font-weight-medium">
                  {{ card.description }}
               </v-card-text>
            </v-card>
         </v-col>
      </v-row>
   </div>
</template>
<style scoped>
.hover-scale {
   transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.hover-scale:hover {
   transform: scale(1.05);
   box-shadow: 0 10px 20px rgb(26, 45, 65);
}
@media screen and (max-width: 960px) {
.v-row {
   flex-wrap: nowrap;
   overflow-x: scroll;
}
   
}

</style>
