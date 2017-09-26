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
article header h1 {
  font-family: 'Oxygen', sans-serif;
}

.content {
  font-family: 'Oxygen', sans-serif;
  font-size: 1.2em;
  margin-left: 10%;
  margin-right:10%;
  line-height: 2em;
  text-align: justify;
}
</style>
