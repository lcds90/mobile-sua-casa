<script setup lang="ts">

interface IProps {
  toggleLeftDrawer: () => void;
}

defineProps<IProps>();

</script>

<template>
  <q-header elevated>
    <q-toolbar>
      <q-btn
        flat
        dense
        round
        icon="menu"
        aria-label="Menu"
        @click="toggleLeftDrawer"
      />
      <q-toolbar-title> Quasar App </q-toolbar-title>
      <div>Quasar v{{ $q.version }}</div>
    </q-toolbar>
  </q-header>
</template>
