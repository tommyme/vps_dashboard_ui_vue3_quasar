<template>
  <div class="q-pa-md">
    <div class="row q-col-gutter-md">
      <div class="col-4">
        <AccountDash></AccountDash>
      </div>
      <div class="col-8">
        <div class="row q-col-gutter-md">
          <div class="col-10">
            <q-card class="my-card q-px-sm" flat bordered>
              <q-toolbar>
                <q-icon name="fas fa-archive" class="q-mr-sm"></q-icon>
                <div class="text-overline q-mr-sm">Voucher</div>
                <q-badge label="8" rounded class="q-mr-sm"></q-badge>
                <q-icon name="fas fa-archive" class="q-mr-sm"></q-icon>
                <div class="text-overline q-mr-sm">Voucher</div>
                <q-badge label="8" rounded class="q-mr-sm"></q-badge>
                <q-icon name="fas fa-archive" class="q-mr-sm"></q-icon>
                <div class="text-overline q-mr-sm">Voucher</div>
                <q-badge label="8" rounded class="q-mr-sm"></q-badge>
                <q-space></q-space>
                <q-btn icon="fas fa-archive" color="green" label="On LEFT"></q-btn>
              </q-toolbar>

            </q-card>
          </div>
          <div class="col-2 row flex-center">
            <q-btn icon="fas fa-ellipsis-h"></q-btn>
          </div>
        </div>

        <h6 class="text-weight-bolder q-ml-lg topTitle">Dashboard</h6>
        <q-toolbar class="topToolbar">
          <div class="text-overline q-mr-sm">My Gameservers</div>
          <q-badge label="9" rounded color="black" class="q-mx-sm"></q-badge>
          <div class="text-overline q-mr-sm">My Gameservers</div>
          <q-badge label="9" rounded color="black" class="q-mx-sm"></q-badge>
          <div class="text-overline q-mr-sm">My Gameservers</div>
          <q-badge label="9" rounded color="black" class="q-mx-sm"></q-badge>
          <q-space></q-space>
          <q-icon name="fas fa-ellipsis-h"></q-icon>
        </q-toolbar>

        <div class="row q-col-gutter-md">

          <div class="col-4" v-for="(_, idx) in range6" :key="idx">
            <q-card class="my-card q-px-sm q-py-lg" flat :style="{ 'background-color': cardColors[idx] }">
              <q-toolbar>
                <q-avatar>
                  <img src="https://cdn.quasar.dev/img/avatar1.jpg" alt="">
                </q-avatar>
                <q-space></q-space>
                <q-badge label="Online" rounded color="green"></q-badge>
              </q-toolbar>
              <div class="text-overline text-weight-bolder q-ml-md">
                Fivem Dev
              </div>
              <div class="text-overline q-ml-md">127.0.0.1:8000</div>
              <q-toolvar>
                <div class="text-overline text-weight-bolder q-ml-sm">
                  21.11.2022
                </div>
                <q-space></q-space>
                <q-btn color="grey" round flat dense :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                  @click="expanded = !expanded"></q-btn>

              </q-toolvar>
              <q-separator></q-separator>
              <q-slide-transition>
                <div v-show="expanded">
                  <q-separator />
                  <q-card-section class="flex flex-center row">
                    <q-icon name="far fa-lightbulb" class="q-mr-md"></q-icon>
                    <q-icon name="far fa-lightbulb" class="q-mr-md"></q-icon>
                    <q-icon name="far fa-lightbulb" class="q-mr-md"></q-icon>
                    <q-icon name="far fa-lightbulb" class="q-mr-md"></q-icon>
                  </q-card-section>


                </div>
              </q-slide-transition>
            </q-card>
          </div>
        </div>




      </div>
    </div>
  </div>
</template>

<script setup>
import AccountDash from 'src/components/AccountDash.vue';
import { ref } from 'vue';
const expanded = ref(false)
const range6 = [0, 0, 0, 0, 0, 0]
const cardColors = [
  "#81ecec",
  "#fab1a0",
  "#a29bfe",
  "#dfe6e9",
  "#ffeaa7",
  "#fdcb6e",
  "#b2bec3",
  "#00b894",
  "#74b9ff",
  "#00cec9",
  "#0984e3",
  "#6c5ce7",
  "#ff7675",
  "#fd79a8",
  "#636e72",
  "#e17055",
  "#d63031",
  "#e84393",
  "#2d3436",
  "#55efc4",
]
</script>

<style scoped>
.topTitle {
  /* margin-top: 10px; */
  margin-top: 2rem;
  margin-bottom: 1rem;
}

.topToolbar {}

.my-card {
  border-radius: 2rem;
}
</style>
