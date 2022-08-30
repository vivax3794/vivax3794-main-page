<template>
  <div class="main_body">
    <div
      v-for="[category, projects] in Object.entries(categories)"
      :key="category"
      :id="category.toLowerCase()"
    >
      <h1
        :style="{
          color: hash === category.toLocaleLowerCase() ? 'yellow' : 'white',
        }"
      >
        {{ category }}
      </h1>
      <n-grid :cols="3" :x-gap="30">
        <n-grid-item v-for="project in projects" :key="project.name">
          <n-card>
            <h2>
              <a :href="project.link">{{ project.name }}</a>
            </h2>
            <p>{{ project.description }}</p>
          </n-card>
        </n-grid-item>
      </n-grid>
    </div>
  </div>
</template>

<script lang="ts" setup>
type Project = {
  name: string;
  description: string;
  link: string;
};

const hash = location.hash.slice(1);

const categories: { [category: string]: Project[] } = {
  Python: [
    {
      name: "Jerde",
      link: "https://pypi.org/project/jerde/",
      description: "Python library for making parsing json structures easier.",
    },
    {
      name: "Arcade Discord Bot",
      link: "https://top.gg/bot/967531303618633740",
      description:
        "Discord bot made in python for playing fun games with friends.",
    },
  ],
  Rust: [
    {
      name: "wave function collapse demo",
      link: "https://vivax.itch.io/wave-generation-demo",
      description:
        "Proof of concept implementation of wave function collapse level generation, using rust and the bevy game engine.",
    },
    {
      name: "Asteroids Clone",
      link: "https://github.com/vivax3794/asteroids",
      description:
        "Clone of the classic asteroids arcade game made in rust using the bevy game engine.",
    },
  ],
  Vue: [
    {
      name: "This site",
      link: "https://github.com/vivax3794/vivax3794-main-page",
      description:
        "This is the site you are currently viewing. \nIt was created using vue and typescript and deployed on cloudflare servers.",
    },
  ],
  Tauri: [
    {
      name: "Supercharged-start",
      link: "https://github.com/vivax3794/supercharged-stars",
      description:
        "Special drawing program for a twitch streamers drawing game, using tauri and vue. Includes custom implementation of k-means for loading images.",
    },
  ],
};
</script>

<style lang="sass" scoped>
@use "sass:math"

.main_body
  position: relative
  $width: 90%
  width: $width
  left: math.div(100% - $width, 2)
</style>
