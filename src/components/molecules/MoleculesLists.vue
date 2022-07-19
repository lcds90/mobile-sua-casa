<script setup lang="ts">
import AtomItem from '../atoms/AtomItem.vue';

interface IProps {
  items: Array<{
    title: string;
    caption: string;
    icon: string;
    link: string;
  }>;
  title: string;
}

defineProps<IProps>();
</script>

<template>
  <q-list>
    <q-item-label header> {{ title }} </q-item-label>
    <AtomItem
      v-for="item in items"
      :key="item.title"
      :item="item"
    />
    <q-separator />
  </q-list>
</template>
