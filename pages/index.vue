<template>
  <section id="posts">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
      :excerpt="post.previewText"
      :thumbnail-image="post.thumbnailUrl"
      :id="post.id"
    />

  </section>

</template>

<script>
import PostPreview from '@/components/Blog/PostPreview.vue'

export default {
  components: { PostPreview },
  asyncData(context) {
    return context.app.$storyapi
      .get('cdn/stories', {
        version: 'draft',
        starts_with: 'blog/'
      })
      .then(res => {
        console.log(res)
        return res
      })
  }
  // data() {
  //   return {
  //     posts: [
  //       {
  //         title: 'Title',
  //         previewText: 'this is awesome text',
  //         thumbnailUrl: 'https://www.w3schools.com/w3images/fjords.jpg',
  //         id: 'title-one'
  //       },
  //
  //       {
  //         title: 'Title twoo',
  //         previewText: 'this is awesome text 2',
  //         thumbnailUrl:
  //           'https://images.ctfassets.net/o59xlnp87tr5/nywabPmH5Y6W4geG8IYuk/0a59905671f8d637350df8e7ec9e7fb9/backgrounds-min.jpg?w=360&h=240&fit=fill',
  //         id: 'title-two'
  //       }
  //     ]
  //   }
  // }
}
</script>
<style scoped>
#posts {
  padding-top: 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: column;
  width: 100%;
}
@media (min-width: 35rem) {
  #posts {
    flex-direction: row;
  }
}
</style>
