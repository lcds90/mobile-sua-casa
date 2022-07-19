<script setup lang="ts">
interface AtomButtonProps {
  onClick: () => void;
  icon: string;
}

defineProps<AtomButtonProps>();

</script>

<template>
  <q-btn
    flat
    dense
    round
    :icon="icon"
    aria-label="Menu"
    @click="onClick"
  />
</template>
