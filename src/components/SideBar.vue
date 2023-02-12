<script setup>
import { ref } from 'vue'

const leftDrawerOpen = ref(false)
const link = ref('user')
</script>

<template>
  <q-drawer show-if-above v-model="leftDrawerOpen" side="left" behavior="desktop" :width="90">
    <div class="flex flex-center q-mb-md bg-brown-2">
      <h6 class="text-weight-bolder">fuck</h6>
    </div>
    <div class="flex flex-center q-my-md column">
      <q-list>
        <q-item clickable :active="'user' === link" @click="link = 'user'" active-class="border">
          <q-item-selection avatar class="flex flex-center">
            <q-icon name="fas fa-user-circle" size="2rem" />
          </q-item-selection>
        </q-item>

        <q-item clickable :active="'doc' === link" @click="link = 'doc'" active-class="border">
          <q-item-selection avatar class="flex flex-center">
            <q-icon name="far fa-file-alt" size="2rem" />
          </q-item-selection>
        </q-item>

        <q-item clickable :active="'shopping' === link" @click="link = 'shopping'" active-class="border">
          <q-item-selection avatar class="flex flex-center">
            <q-icon name="fas fa-shopping-basket" size="2rem" />
          </q-item-selection>
        </q-item>

        <q-item clickable :active="'search' === link" @click="link = 'search'" active-class="border">
          <q-item-selection avatar class="flex flex-center">
            <q-icon name="fas fa-search" size="2rem" />
          </q-item-selection>
        </q-item>
      </q-list>
    </div>
    <div style="position: absolute; bottom: 20px; left: 0px; right: 0px; text-align: center">
      <div class="text-overline">EUR</div>
      <div class="text-overline">US</div>
    </div>
  </q-drawer>

</template>



<style scoped>
.border {
  background-color: #93c99c;
}

.q-item {
  border-radius: 50%;
  margin: 16px 16px !important;
  padding: 8px 8px !important;
}
</style>
