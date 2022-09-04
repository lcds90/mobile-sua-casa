<script setup lang="ts">
import { MoleculeForm } from 'src/components';

interface IFormData {
  label: string,
  type: string,
  value: any,
  hint?: string,
  rules?: any[]
}

interface IProps {
  onSubmit: any,
  onReset: any,
  data: IFormData[]
}

defineProps<IProps>();

</script>

<template>
    <div class="q-pa-md container">
      <molecule-form :onSubmit="onSubmit" :onReset="onReset" :data="data" />
    </div>
</template>

<style scoped>
.container {
  background: rgba(0, 0, 0, 0.05);
  box-shadow: 0 5px 5px rgba(0, 0, 0, 0.15);
  width: 75%;
}
</style>
