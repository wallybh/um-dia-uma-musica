<template>
  <main>
    <post v-for="post in posts"
      v-bind:key="post.id"
      v-bind:title="post.title"
      v-bind:content="post.content">
    </post>
  </main>
</template>

<script>
import post from './Post';

export default {
  name: 'posts',
  data() {
    return {
      posts: [
        {
          id: 1,
          title: 'Fuck World!',
          content: 'My second blog post! Fuck my life!',
        },
        {
          id: 0,
          title: 'Hello world!',
          content: 'My first blog post! Fuck world!',
        },
      ],
    };
  },
  components: {
    post,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
