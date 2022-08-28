<template>
  <n-menu :options="options" />
</template>

<script lang="tsx" setup>
import { NIcon, type MenuOption } from "naive-ui";
import { RouterLink } from "vue-router";
import { BookOutline as BookIcon } from "@vicons/ionicons5";

const options: MenuOption[] = [
  {
    label: () => <RouterLink to={{ name: "home" }}>Home</RouterLink>,
    icon: () => (
      <NIcon>
        <BookIcon />
      </NIcon>
    ),
  },
];
</script>
