<template>
  <div>
    <svg class="header-bg-svg" :viewbox="vb" height="217" width="100%" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none">
      <path :d="pd1" fill-opacity=".8" fill="#18D060"></path>
      <path :d="pd2" fill="#FFF"></path>
    </svg>
    <pre>{{ vb }}</pre>
    <h1>About</h1>
    <nuxt-link to="/">Nuxt-link Home page</nuxt-link>
    <br>
    <a href="/">Normal link Home page</a>
  </div>
</template>

<script>
export default {
  head: {
    bodyAttrs: {
      class: 'red'
    }
  },
  data() {
    return {
      vb: '0 0 1680 217',
      pd1: 'M0 171V0h1680v171S554.21 222.169 256.791 216.148C79.484 212.558 0 171 0 171z',
      pd2: 'M0 161V0h1680v161S554.21 195.169 256.791 189.148C79.484 185.558 0 161 0 161z',
    }
  },
  created() {
    if (process.browser) {
      window.addEventListener('resize', this.handler, {passive: true});
      this.vb = `0 0 ${window.innerWidth} 217`;
      this.pd1 = `M0 171V0h${window.innerWidth}v171S554.21 222.169 256.791 216.148C79.484 212.558 0 171 0 171z`
      this.pd2 = `M0 161V0h${window.innerWidth}v161S554.21 195.169 256.791 189.148C79.484 185.558 0 161 0 161z`
    }
  },
  methods: {
    handler() {
      this.vb = `0 0 ${window.innerWidth} 217`;
      this.pd1 = `M0 171V0h${window.innerWidth}v171S554.21 222.169 256.791 216.148C79.484 212.558 0 171 0 171z`
      this.pd2 = `M0 161V0h${window.innerWidth}v161S554.21 195.169 256.791 189.148C79.484 185.558 0 161 0 161z`
    }
  },
}
</script>

<style>
.red {
  background: red;
}
a, h1 {
  color: white;
}
</style>
