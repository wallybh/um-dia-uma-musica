<template>
  <article>
    <header>
      <h1>{{title}}</h1>
    </header>
    <div class="content">
      {{content}}
    </div>
    <hr>
  </article>
</template>

<script>
export default {
  name: 'Post',
  props: ['title', 'content'],
};
</script>

<style>

</style>
