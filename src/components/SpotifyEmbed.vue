<template>
  <iframe :src="src" :width="width" :height="height" frameborder="0" allowtransparency="true">
  </iframe>
</template>
<script>
export default {
  name: 'spotify',
  props: {
    spotifyUri: {
      type: String,
      required: true,
    },
    width: {
      type: Number,
      default: 300,
    },
    height: {
      type: Number,
      default: 80,
    },
  },
  // props: ['spotifyUri'],
  data: function data() {
    return {
      src: `https://open.spotify.com/embed?uri=${this.spotifyUri}`,
    };
  },
};
</script>

<style>

</style>
