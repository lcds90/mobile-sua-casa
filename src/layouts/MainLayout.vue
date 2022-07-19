<script setup lang="ts">
import { ref } from 'vue';
import { OrganismDrawer, OrganismHeader } from 'src/components';
import { useMetaStore } from 'src/stores/meta';

const meta = useMetaStore();

const leftDrawerOpen = ref(false);

const toggleLeftDrawer = () => {
  leftDrawerOpen.value = !leftDrawerOpen.value;
};

</script>

<template>
  <q-layout view="lHh Lpr lFf">
    <organism-header :toggle-left-drawer="toggleLeftDrawer" />
    <organism-drawer
      :left-drawer-open="leftDrawerOpen"
      :items="meta.linksList"
    />
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>
