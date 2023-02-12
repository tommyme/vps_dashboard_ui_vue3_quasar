<script setup>
import { ref } from 'vue';
import ClickableIconWordItem from './items/ClickableIconWordItem.vue';

const link = ref('Dashboard')
window.xxx = () => {
  console.log
}
</script>

<template>
  <q-card class="my-card q-pa-sm colorCard" flat :height="300">
    <h6 class="text-weight-bolder q-ml-lg">Account</h6>
    <q-list>
      <ClickableIconWordItem :bindTarget="link" name="Dashboard" icon="fas fa-tachometer-alt"
        @click="() => { link = 'Dashboard' }" />
      <ClickableIconWordItem :bindTarget="link" name="Cashbox" icon="fas fa-box-open"
        @click="() => { link = 'Cashbox' }" />
      <ClickableIconWordItem :bindTarget="link" name="Contact" icon="fas fa-box-open"
        @click="() => { link = 'Contact' }" />
      <ClickableIconWordItem :bindTarget="link" name="Cash" icon="fas fa-box-open" @click="() => { link = 'Cash' }" />
      <ClickableIconWordItem :bindTarget="link" name="Orders" icon="fas fa-box-open" @click="() => { link = 'Orders' }">
        <q-badge label="3" color="green"></q-badge>
      </ClickableIconWordItem>

    </q-list>

  </q-card>

</template>

<style scoped lang="scss">
.colorCard {
  background: #f6f8f7;
  height: 660px;
  border-radius: 25px;
}

.q-item__section--avatar {
  color: black !important;
}


.styleme {
  margin-left: 165px;
}
</style>
