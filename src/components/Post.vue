<template>
  <article>
    <hr>
    <header>
      <h1>{{title}}</h1>
    </header>
    <div class="content">
      <youtube class="video-wrapper" v-if="videoId" :video-id="videoId"></youtube>
      <spotify v-if="spotifyUri" :spotify-uri="spotifyUri"></spotify>
      {{content}}
    </div>
  </article>
</template>

<script>
import spotify from './SpotifyEmbed';

export default {
  name: 'Post',
  props: ['title', 'content', 'videoId', 'spotifyUri'],
  components: {
    spotify,
  },
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
  margin-right: 10%;
  line-height: 2em;
  text-align: justify;
}

article hr {
  margin-left: 10%;
  margin-right: 10%;
}

main article:first-child hr {
  display: none;
}

.video-wrapper {
	position: relative;
  text-align: center;
  padding-bottom: 56.25%; /* 16:9 */
	overflow: hidden;
	height: 0;
}
.video-wrapper iframe {
	position: absolute;
	top: 0;
	left: 0;
  width: 100%;
  height: 100%;
}
</style>
