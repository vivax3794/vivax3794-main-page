<template>
  <n-menu :options="options" mode="horizontal" />
</template>

<script lang="tsx" setup>
import { NIcon, type MenuOption } from "naive-ui";
import { RouterLink } from "vue-router";
import {
  HomeOutline as HomeIcon,
  GitBranchOutline as ProjectIcon,
} from "@vicons/ionicons5";

const options: MenuOption[] = [
  {
    label: () => <RouterLink to={{ name: "home" }}>Home</RouterLink>,
    icon: () => (
      <NIcon>
        <HomeIcon />
      </NIcon>
    ),
  },
  {
    label: () => <RouterLink to="/projects">Project</RouterLink>,
    icon: () => (
      <NIcon>
        <ProjectIcon />
      </NIcon>
    ),
  },
];
</script>
