<template>
  <div>
    <the-header/>
    <main class="mai-content">
      <nuxt/>
    </main>
  </div>
</template>

<script>
import TheHeader from '@/components/TheHeader/TheHeader.vue'

export default {
  components: {
    TheHeader
  }
}
</script>

<style>
body {
  background: lightblue;
  font-family: 'Oswald', sans-serif;
}

h1 {
  font-family: 'Oswald', sans-serif;
}
* {
  box-sizing: border-box;
}
a {
  text-decoration: none;
}
.main-content {
  background-color: #7f828b;
}
</style>
