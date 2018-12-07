<template>
  <nuxt-link
    :to="id">
    <article class="post-preview">
      <div
        :style="{ backgroundImage: 'url(' + thumbnailImage + ')'}"
        class="post-preview-thumbnail"/>
      <div class="post-preview-content">
        <h1>{{ title }}</h1>
        <p> {{ excerpt }}</p>
      </div>
    </article>
  </nuxt-link>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    excerpt: {
      type: String,
      required: true
    },
    thumbnailImage: {
      type: String,
      required: true
    },
    id: {
      type: String,
      required: true
    }
  }
}
</script>
<style scoped>
a {
  color: darkolivegreen;
}
h1 {
  color: coral;
}

.post-preview {
  width: 400px;
  background-color: lightgoldenrodyellow;
  box-shadow: 1px 1px 1px 1px rgba(0, 0, 210, 0.5);
  margin-bottom: 10px;
  margin-top: 10px;
  margin-left: auto;
  margin-right: auto;
}
.post-preview-thumbnail {
  background-position: center;
  -webkit-background-size: cover;
  background-size: cover;
  width: 100%;
  height: 10rem;
  margin: auto;
}
.post-preview-content {
  text-align: center;
  padding: 1rem;
}
</style>
