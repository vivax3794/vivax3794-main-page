<template>
  <h1 class="no_margin">
    <n-gradient-text
      :gradient="{
        from: '#f800fc',
        to: '#05f0fc',
        deg: 90,
      }"
    >
      Hello World!
    </n-gradient-text>
  </h1>
  <p>I am vivax, I do programming!</p>
  <div id="cards">
    <n-grid :x-gap="100" :y-gap="50" :cols="3">
      <n-grid-item>
        <n-card>
          <h2 class="no_margin">Languages</h2>
          <ul>
            <li>
              <RouterLink to="/projects#python" id="python" class="list_item">
                <img src="/imgs/python-logo.png" class="logo" />Python
              </RouterLink>
            </li>
            <li>
              <RouterLink to="/projects#rust" id="rust" class="list_item">
                <img
                  src="/imgs//rust-logo.svg"
                  class="logo"
                  :style="{ filter: 'invert(100%)' }"
                />Rust
              </RouterLink>
            </li>
            <li>
              <RouterLink
                to="/projects#typescript"
                id="typescript"
                class="list_item"
              >
                <img src="/imgs//ts-logo-128.png" class="logo" />Typescript
              </RouterLink>
            </li>
          </ul>
        </n-card>
      </n-grid-item>
      <n-grid-item>
        <n-card>
          <h2 class="no_margin">Tech</h2>
          <ul>
            <li>
              <RouterLink to="/projects#vue">
                <a class="list_item" id="vue"
                  ><img src="/imgs//vue.png" class="logo" />Vue</a
                >
              </RouterLink>
            </li>
            <li>
              <RouterLink to="/projects#tauri">
                <a class="list_item" id="tauri"
                  ><img src="/imgs//tauri-logo.png" class="logo" />Tauri</a
                >
              </RouterLink>
            </li>
            <li><a class="list_item" id="mongodb">MongoDB</a></li>
          </ul>
        </n-card>
      </n-grid-item>
      <n-grid-item>
        <n-card>
          <h2 class="no_margin">Socials</h2>
          <ul>
            <li>
              <a
                href="https://twitch.tv/vivax3794"
                class="list_item"
                id="twitch"
              >
                <img src="/imgs//twitch-logo.jpg" class="logo" />Twitch
              </a>
            </li>
            <li>
              <a
                href="https://github.com/vivax3794"
                class="list_item"
                id="github"
              >
                <img src="/imgs//github-logo.png" class="logo" />Github
              </a>
            </li>
            <li>
              <a
                href="https://www.codingame.com/profile/77e99ab38d5b1d335bbebafa23edbdd66293053"
                class="list_item"
                id="codingame"
                >CodinGame
              </a>
            </li>
          </ul>
        </n-card>
      </n-grid-item>
    </n-grid>
  </div>
</template>

<style lang="sass" scoped>
@use "sass:math"

#cards
  $width: 70%
  width: $width
  margin-left: math.div(100% - $width, 2)

.no_margin
  margin-bottom: 0px
  margin-top: 0px

h1
  font-size: 90px
  text-align: center

h2
  font-size: 50px

p
  margin-top: 0px
  margin-bottom: 100px
  font-size: 25px
  text-align: center

$animation_time: 200ms

ul
  list-style-type: none

.logo
  width: 30px
  transition: width $animation_time ease-out
  vertical-align: middle
  margin-right: 10px

a
  text-decoration: none

a:visited
  color: white

.list_item
  color: white
  font-size: 20px
  transition: font-size $animation_time ease-out, color $animation_time

.list_item:hover
  font-size: 30px
  text-decoration: underline

  > .logo
    width: 40px

// TEXT COLORS
#python:hover
  color: #FFE873

#rust:hover
  color: #f74c00

#typescript:hover
  color: #3178c6

#twitch:hover
  color: #6445a2

#github:hover
  color: #4183C4

#codingame:hover
  color: #fcd207

#vue:hover
  color: #41b883

#tauri:hover
  color: #25d3e8

#mongodb:hover
  color: #3fa037
</style>
