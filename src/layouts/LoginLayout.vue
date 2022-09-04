<template>
  <q-layout view="hHh lpR fFf">

    <q-page-container class="login-layout">
      <router-view />
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar>
          <div>Title</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<style scoped>
.login-layout {
  height: 100vh;
  overflow-y: auto;
  display: grid;
  place-items: center;
}
</style>
