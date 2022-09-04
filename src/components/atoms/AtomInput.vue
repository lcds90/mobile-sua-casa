<script setup lang="ts">
import { ValidationRule } from 'quasar';
import { ref } from 'vue';

interface IProps {
  label: string,
  type: string,
  value: string | number,
  hint?: string,
  rules?: ValidationRule[]
}

const props = defineProps<IProps>();
const value = ref(props.value);
</script>

<template>
  <q-input
        v-model="value"
        filled
        :hint="hint"
        :label="label"
        lazy-rules
        :rules="rules"
  />
</template>
