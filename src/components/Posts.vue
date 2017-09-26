<template>
  <main>
    <post v-for="post in posts"
      v-bind:key="post.id"
      v-bind:title="post.title"
      v-bind:content="post.content"
      v-bind:videoId="post.videoId">
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
          id: 2,
          title: 'First ride',
          friendlyName: 'first-ride',
          content: 'Ultimamente estou gostando muito  músicas instrumentais. Músicas com uma pegada mais calma. Tenho uma playlist onde coloco as minhas músicas favoritas e de vez em quando eu procuro algo novo para incrementá-la. Hoje eu conheci a música First ride. Ouvir essa música foi como ouvir o violão conversar diretamente comigo. Como se ele tivesse me contando uma história.',
          videoId: '170GfcR1i_A',
        },
        {
          id: 1,
          title: 'Fuck World!',
          friendlyName: 'fuck-world',
          content: 'My second blog post! Fuck my life!',
        },
        {
          id: 0,
          title: 'Hello world!',
          friendlyName: 'hello-world',
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
