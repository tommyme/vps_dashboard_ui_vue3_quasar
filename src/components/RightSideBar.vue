<script setup>
import { ref } from 'vue';

const rightDrawerOpen = ref(true)
</script>

<template>
  <q-drawer show-if-above v-model="rightDrawerOpen" side="right" behavior="desktop" bordered :width="300">
    <div style="width: 100%; height: 100%;" class="flex column">

      <q-list>
        <q-toolbar class="q-mt">
          <q-icon name="far fa-question-circle" class="q-mr-sm"></q-icon>
          <q-icon name="far fa-caret-square-right"></q-icon>
          <q-space></q-space>
          <q-icon name="fa-solid fa-cloud" class="q-mr-sm"></q-icon>
          <div class="text-overline">Online</div>
        </q-toolbar>
        <div class="flex flex-center column user-item">
          <!-- item row -->
          <q-item class="flex flex-center">
            <q-item-section avatar>
              <q-avatar rounded>
                <img src="https://cdn.quasar.dev/img/boy-avatar.png">
              </q-avatar>
            </q-item-section>
            <q-item-section>
              <div class="flex flex-center">
                <q-text class="text-weight-bold">shellcode flag</q-text>
                <q-badge color="green" rounded class="q-mx-sm"></q-badge>
                <q-icon name="fas fa-chevron-down" color="grey"></q-icon>
              </div>
              <q-text class="text-weight-light">flag3455</q-text>
            </q-item-section>
          </q-item>
          <div class="flex flex-center q-my-md">
            <q-text class="text-h6 text-weight-bolder">150,080,30 $</q-text>
            <q-icon name="fas fa-plus-circle" color="green" class="q-ml-md"></q-icon>
          </div>
        </div>
        <q-separator />
        <q-toolbar>
          <q-icon name="fas fa-info-circle" color="" class="q-mr-sm"></q-icon>
          <div class="text-overline">coins</div>
        </q-toolbar>
        <div class="flex flex-center column q-pa-sm">
          <q-linear-progress rounded :value="0.69" size="20px" />
          <q-toolbar>
            <div class="text-overline">Storage</div>
            <q-space></q-space>
            <div class="text-overline">69%</div>
          </q-toolbar>
        </div>
      </q-list>
      <div>

        <q-toolbar>
          <q-icon name="far fa-hdd" class="q-mr-sm"></q-icon>
          <div class="text-overline">partner menu</div>
        </q-toolbar>
        <q-separator />
        <q-toolbar>
          <q-icon name="far fa-hdd" class="q-mr-sm"></q-icon>
          <div class="text-overline">partner menu</div>
        </q-toolbar>
        <q-toolbar>
          <q-icon name="far fa-hdd" class="q-mr-sm"></q-icon>
          <div class="text-overline">partner menu</div>
        </q-toolbar>
        <q-toolbar>
          <q-icon name="far fa-hdd" class="q-mr-sm"></q-icon>
          <div class="text-overline">partner menu</div>
        </q-toolbar>
        <q-toolbar>
          <q-icon name="far fa-hdd" class="q-mr-sm"></q-icon>
          <div class="text-overline">partner menu</div>
        </q-toolbar>
        <q-toolbar>
          <q-icon name="far fa-hdd" class="q-mr-sm"></q-icon>
          <div class="text-overline">partner menu</div>
        </q-toolbar>
      </div>
      <div style="flex-grow: 1;"></div>
      <q-toolbar style="flex-direction: row-reverse;">
        <q-icon name="facebook" class="q-px-sm" style="font-size: 2rem;" />
        <q-icon name="facebook" class="q-px-sm" style="font-size: 2rem;" />
        <div class="q-px-sm overline">quick news</div>
      </q-toolbar>
    </div>



  </q-drawer>
</template>

<style scoped>

</style>
