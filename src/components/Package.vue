<script setup>
import { ref } from "vue";
import packageData from "../stores/AIDevTool.json";
const model = ref(null);
const slides = ["First", "Second", "Third", "Fourth", "Fifth"];
</script>
<template>
   <div class="container d-flex justify-center flex-column">
      <div class="text-h4 text-center font-weight-bold align-self-center py-3">套件服務</div>
      <v-divider class="border-opacity-75 ma-auto" :thickness="4" width="60%"></v-divider>
      <div class="text-subtitle-1 text-center py-3 font-weight-medium">
         AI開發套件-提供眾多AI開發框架及IDE，快速構建所需的環境。
      </div>
      <v-carousel class="py-5" delimiter-icon="mdi-square"  height="650"
    show-arrows="hover" cycle hide-delimiter-background>
         <v-carousel-item v-for="(devtool, i) in packageData" :key="i">
            <v-container class="bg-surface-variant">
               <v-hover v-slot="{ isHovering, props }">
                  <v-card class="mx-auto bg-surface-light" color="grey-lighten-4" max-width="600" v-bind="props">
                     <v-img :aspect-ratio="16 / 9" :src="`./icons/${devtool.img}`">
                        <v-expand-transition>
                           <div v-if="isHovering" class="d-flex bg-orange-darken-2 v-card--reveal" style="height: 100%">
                              <div class="ma-5 text-subtitle-1">
                                 {{ devtool.introduction }}
                              </div>
                           </div>
                        </v-expand-transition>
                     </v-img>

                     <v-card-text class="pt-6 text-center">
                        <h3 class="text-h4 font-weight-medium text-blue-grey-darken-3 mb-2">
                           {{ devtool.title }}
                        </h3>
                     </v-card-text>
                  </v-card>
               </v-hover>
            </v-container>
         </v-carousel-item>
      </v-carousel>
   </div>
</template>
<style scoped>
.v-card--reveal {
   align-items: center;
   bottom: 0;
   justify-content: center;
   opacity: 0.9;
   width: 100%;
}
</style>
