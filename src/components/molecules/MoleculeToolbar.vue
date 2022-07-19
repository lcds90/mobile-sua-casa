<script setup lang="ts">
import { AtomButton } from 'src/components';

interface IAtomToolbarProps {
  onClick: () => void;
  title: string;
  text: string;
}

defineProps<IAtomToolbarProps>();

</script>

<template>
  <q-toolbar>
    <atom-button
      icon="menu"
      :onClick="onClick"
    />
    <transition
      appear
      enter-active-class="animated fadeInRight delay5s"
      leave-active-class="animated fadeOut"
    >
      <q-toolbar-title> {{ title }} </q-toolbar-title>
    </transition>
    <div> {{ text }}</div>
  </q-toolbar>
</template>

<style scoped>
.delay5s {
  animation-duration: 5s;
}
</style>
