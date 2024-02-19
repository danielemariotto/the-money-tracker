<script setup>
import { ref } from 'vue';
const menuselected = ref('')
import DailyViewVue from '@/views/DailyView.vue'

</script>

<template>
  <v-layout class="rounded rounded-md">
    <v-app-bar title="Track expenses"></v-app-bar>

    <v-navigation-drawer>
      <v-list>
        <v-list-item @click="menuselected='Track expenses'" title="Track expenses"></v-list-item>
        <v-list-item @click="menuselected='Future Transaction'" title="Future Transaction"></v-list-item>
        <v-list-item @click="menuselected='Recurring Transaction'" title="Recurring Transaction"></v-list-item>

      </v-list>
    </v-navigation-drawer>
    <v-main v-if="menuselected==='Track expenses'" class="d-flex align-center justify-center" style="min-height: 300px;">
      <DailyViewVue/>
    </v-main>

    <v-main v-if="menuselected==='Future Transaction'" class="d-flex align-center justify-center" style="min-height: 300px;">
      2
    </v-main>

    <v-main v-if="menuselected==='Recurring Transaction'" class="d-flex align-center justify-center" style="min-height: 300px;">
      3
    </v-main>
  </v-layout>

</template>

<style scoped>

</style>
