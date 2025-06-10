<script setup></script>

<template>
   <!-- <v-sheet class="pa-16" max-width="100%" color="#192c44" :elevation="15"> -->
   <div class="container d-flex justify-center flex-column">
      <div class="text-h4 text-center font-weight-bold align-self-center py-3">聯絡資訊</div>
      <v-divider class="border-opacity-75 ma-auto" :thickness="4" width="60%"></v-divider>
      <div class="text-subtitle-1 text-center py-3 font-weight-medium mb-6">歡迎與我們聯繫</div>
      <v-container class="mt-2">
         <v-row class="d-flex flex-wrap">
            <v-col md="6" class="pa-2 ma-2">
               <div class="left-container mb-6">
                  <div class="text-h6">科技公司</div>
                  <p class="pt-4">
                     ucan是一家專注於人工智慧運算的科技公司，致力於為各行各業提供高效、智慧的解決方案。憑藉先進的演算法和強大的運算能力，我們協助企業提升決策效率，優化業務流程，推動創新發展。
                  </p>
               </div>
               <div class="left-container mb-6">
                  <div class="text-h6">聯絡資訊</div>
                  <div class="contact_link_box pt-3">
                     <a
                        class="text-decoration-none text-white"
                        href="https://maps.app.goo.gl/GrJ2bVuX1EorsRAH9"
                        target="_blank"
                     >
                        <v-icon icon="mdi-map-marker" class="pr-2 mr-2" />
                        <span>Google地址</span>
                     </a>
                     <a>
                        <v-icon icon="mdi-phone" class="mr-2" />
                        <span>02-22222222</span>
                     </a>
                     <a
                        class="text-decoration-none text-white"
                        href="mailto:softwareservice@besta.com.tw"
                        target="_blank"
                        rel="nofollow noreferrer"
                     >
                        <v-icon icon="mdi-email" class="mr-2" />
                        <span>softwareservice@ucan.com.tw</span>
                     </a>
                  </div>
               </div>
            </v-col>
            <!-- <v-spacer></v-spacer> -->
            <v-col class="pa-2 ma-2 align-self-center">
               <img style="max-width: 100%; max-height: 100%" src="../../public/icons/free-logo.png" alt="free-logo" />
            </v-col>
         </v-row>
      </v-container>
   </div>

   <v-sheet>
      <p class="pa-3 text-center">
         &copy;
         <span id="displayYear"></span>
         UCAN
         <a
            class="text-decoration-none"
            href="https://www.notion.so/20e49c81e43a80ffbcd8f6b330a7239c?source=copy_link"
            target="_blank"
            >Ucan</a
         >
         Co., Ltd. All rights reserved.
      </p>
   </v-sheet>
</template>

<style scoped>
.contact_link_box {
   display: flex;
   flex-direction: column;
   height: 15vh;
   justify-content: space-between;
}
.contact_link_box a:hover {
   color: aquamarine !important;
}
</style>
