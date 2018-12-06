<template>
  <div id="post">
    <div class="post-thumbnail">s</div>
    <h1>s</h1>
    <p>s</p>
  </div>
</template>
<script>
export default {
  asyncData(context) {
    return context.app.$storyapi
      .get('cdn/stories/' + context.params.postId, {
        version: 'draft'
      })
      .then(res => {
        console.log(res.data)
      })
  }
}
</script>
