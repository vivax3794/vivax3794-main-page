<template>
  <n-card id="body">
    <h1>
      <n-gradient-text
        :gradient="{
          from: '#f800fc',
          to: '#05f0fc',
          deg: 90,
        }"
        >Hello World</n-gradient-text
      >
    </h1>
    <p>I am vivax, I do programming!</p>
  </n-card>
</template>

<style lang="sass" scoped>
@use "sass:math"

#body
  $width: 70%
  width: $width
  left: math.div(100% - $width, 2)

h1
  font-size: 60px
  text-align: center

p
  font-size: 25px
  text-align: center
</style>
