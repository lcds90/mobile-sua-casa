<script setup lang="ts">
interface AtomButtonProps {
  onClick?: () => void;
  icon: string;
  label?: string;
  type?: string;
  color?: string;
  round?: boolean;
}

withDefaults(defineProps<AtomButtonProps>(), {
  round: false,
});

</script>

<template>
  <q-btn
    flat
    dense
    :round="round"
    :color="color"
    :icon="icon"
    aria-label="Menu"
    @click="onClick"
    :type="type"
    :label="label"
  />
</template>
