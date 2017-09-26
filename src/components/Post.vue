<template>
  <article>
    <header>
      <h1>{{title}}</h1>
    </header>
    <div class="content">
      <youtube v-if="videoId" :video-id="videoId"></youtube>
      {{content}}
    </div>
    <hr>
  </article>
</template>

<script>
export default {
  name: 'Post',
  props: ['title', 'content', 'videoId'],
};
</script>

<style>
</style>
