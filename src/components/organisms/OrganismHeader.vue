<script setup lang="ts">
import { MoleculeToolbar } from 'src/components';

interface IProps {
  toggleLeftDrawer: () => void,
}

defineProps<IProps>();

</script>

<template>
  <q-header elevated>
    <molecule-toolbar
      :onClick="toggleLeftDrawer"
      title="Quasar app"
      :text="`Quasar v ${$q.version}`"
    />
  </q-header>
</template>
