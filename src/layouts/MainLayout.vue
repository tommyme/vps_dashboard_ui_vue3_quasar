<template>
  <q-layout view="lHh Lpr lFf">
    <SideBar />
    <RightSideBar />


    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import SideBar from 'components/SideBar.vue'
import RightSideBar from 'src/components/RightSideBar.vue';
import { ref } from 'vue'
</script>
