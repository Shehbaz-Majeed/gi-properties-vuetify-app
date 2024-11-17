<template>
  <v-app>
    <Header />
    <v-main class="main-div-sm">
      <router-view />
    </v-main>
    <Footer />
  </v-app>
</template>

<script setup lang="ts">
  import Header from '@/components/Header.vue'
</script>