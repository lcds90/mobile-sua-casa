<script setup lang="ts">
import { computed } from 'vue';
import MoleculesLists from '../molecules/MoleculesLists.vue';

interface IProps {
  leftDrawerOpen: boolean;
  items: Array<{
    title: string;
    caption: string;
    icon: string;
    link: string;
  }>;
}

const props = defineProps<IProps>();

const leftDrawerOpen = computed(() => props.leftDrawerOpen);
</script>

<template>
  <q-drawer
    v-model="leftDrawerOpen"
    bordered
  >
    <molecules-lists
      :items="items"
      title="Teste"
    />
  </q-drawer>
</template>
