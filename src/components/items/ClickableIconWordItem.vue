<script setup>
import { ref } from 'vue';
const props = defineProps(['bindTarget', 'name', 'icon'])

</script>

<template>
  <q-item clickable :active="bindTarget === name" active-class="actived text-green" class="q-my-md">
    <q-item-section avatar class="flex-center">
      <q-icon :name="icon"></q-icon>
    </q-item-section>

    <q-item-section>
      <div>{{ name }}</div>
    </q-item-section>

    <q-item-section side class="row justify-end items-center" style="position: relative;">
      <div style="position: absolute; left:100%">
        <slot></slot>
      </div>

    </q-item-section>
  </q-item>
</template>

<style scoped>
.actived {
  background: #b3e3bb;
  border-radius: 1rem;
}

q-icon {
  font-size: 1.5rem;
}
</style>
