<template>
    <header>
      <span>{{appName}}</span>
    </header>
</template>

<script>
export default {
  name: 'app-header',
  props: ['offset'],
  data() {
    return {
      appName: 'Um dia, uma música',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  position: fixed;
  display: flex;
  top: 0;
  left: 0;
  margin: 0;
  height: 56px;
  width: 100%;
  padding: 0 16px 0 24px;
  background-color: rgba(53, 73, 94, 0.5);
  color: #ffffff;
}

header span {
  display: block;
  position: relative;
  font-size: 20px;
  line-height: 1;
  letter-spacing: .02em;
  font-weight: 400;
  box-sizing: border-box;
  padding-top: 16px;
}
</style>
