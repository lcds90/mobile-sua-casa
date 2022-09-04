<script setup lang="ts">
import { OrganismLoginForm } from 'src/components';
import { useQuasar, ValidationRule } from 'quasar';
import { reactive } from 'vue';

interface IFormData {
  label: string,
  type: string,
  value: string | number | null,
  hint?: string,
  rules?: ValidationRule[]
}

const user = reactive<IFormData>({
  label: 'Seu e-mail',
  hint: 'E-mail cadastrado',
  type: 'email',
  value: null,
  rules: [
    (val: string) => (val !== null && val !== '') || 'Por favor digite um e-mail',
    (val: string) => val.includes('@') || 'Por favor digite um e-mail válido',
  ],
});

const password = reactive<IFormData>({
  label: 'Sua senha',
  hint: 'Senha do cadastro',
  type: 'text',
  value: null,
  rules: [
    (val: string) => (val !== null && val !== '') || 'Por favor digite a sua senha',
    (val: string) => val.length > 8 || 'Por favor digite uma senha válida',
  ],
});

const data: IFormData[] = [user, password];

const $q = useQuasar();

const onSubmit = () => {
  $q.notify({
    color: 'green-4',
    textColor: 'white',
    icon: 'cloud_done',
    message: 'Submitted',
  });
};

const onReset = () => {
  user.value = null;
  password.value = null;
};
</script>

<template>
    <organism-login-form :data="data" :onSubmit="onSubmit" :onReset="onReset" />
</template>
