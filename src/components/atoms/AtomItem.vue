<script setup lang="ts">
interface IProps {
  item: {
    title: string;
    caption: string;
    icon: string;
    link: string;
  };
}

defineProps<IProps>();
</script>

<template>
  <q-item
    clickable
    v-ripple
    :key="item.title"
    v-bind="item"
  >
    <q-item-section avatar>
      <q-icon
        color="primary"
        name="bluetooth"
      />
    </q-item-section>
    <q-item-section>{{ item.title }}</q-item-section>
  </q-item>
</template>
