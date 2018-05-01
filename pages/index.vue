<template>
  <div>
    <svg class="header-bg-svg" viewbox="0 0 1680 217" height="217" width="100%" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none">
      <path d="M0 171V0h1680v171S554.21 222.169 256.791 216.148C79.484 212.558 0 171 0 171z" fill-opacity=".8" fill="#18D060"></path>
      <path d="M0 161V0h1680v161S554.21 195.169 256.791 189.148C79.484 185.558 0 161 0 161z" fill="#FFF"></path>
    </svg>
    <svg v-if="show" class="header-bg-svg" viewbox="0 0 1680 217" height="217" width="100%" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none">
      <path d="M0 171V0h1680v171S554.21 222.169 256.791 216.148C79.484 212.558 0 171 0 171z" fill-opacity=".8" fill="#18D060"></path>
      <path d="M0 161V0h1680v161S554.21 195.169 256.791 189.148C79.484 185.558 0 161 0 161z" fill="#FFF"></path>
    </svg>
    <button type="button" @click="show = !show">Toggle v-if</button>
    <h1>Home</h1>
    <nuxt-link to="/about">Nuxt-link About page</nuxt-link>
    <br>
    <a href="/about">Normal link About page</a>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
    }
  }
}
</script>

<style>
body {
  background: black;
}
a, h1 {
  color: white;
}
</style>
