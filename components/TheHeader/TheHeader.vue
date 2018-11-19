<template>
  <header class="main-header">
    <nav class="main-nav">
      <ul class="nav-links">
        <nuxt-link 
          to="/" 
          tag="li"><a >All Posts </a> </nuxt-link>
        <nuxt-link
          to="/about"
          tag="li"><a > About </a></nuxt-link>
      </ul>
    </nav>

  </header>
</template>

<style scoped>
.main-header {
  background-color: #1f1f27;
  width: 100%;
  height: 60px;
  display: flex;
}
.nav-links {
  display: flex;
  justify-content: space-between;
  list-style: none;
}
.nav-links li {
  min-width: 100px;
  color: #47494e;
}
a {
  color: #3e3ea5;
}

.nav-link.nuxt-link-exact-active {
  border-bottom: 3px solid deeppink;
}

a:active,
a:hover,
li.nuxt-link-exact-active a {
  color: #59b9e4;
}
</style>
