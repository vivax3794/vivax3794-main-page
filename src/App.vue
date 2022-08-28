<template>
  <n-config-provider :theme="darkTheme">
    <n-global-style />
    <n-layout>
      <n-layout-header>
        <v-navbar />
      </n-layout-header>
      <n-layout-content>
        <router-view />
      </n-layout-content>
    </n-layout>
  </n-config-provider>
</template>

<script setup lang="ts">
import { darkTheme } from "naive-ui";
</script>
