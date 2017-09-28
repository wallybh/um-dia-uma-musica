<template>
  <main>
    <post v-for="post in posts"
      v-bind:key="post.id"
      v-bind:title="post.title"
      v-bind:content="post.content"
      v-bind:videoId="post.videoId"
      :spotify-uri="post.spotifyUri">
    </post>
  </main>
</template>

<script>
import post from './Post';
import fakePosts from '../fake-posts';

export default {
  name: 'posts',
  data() {
    return {
      posts: fakePosts,
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
