<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      <a href="https://www.youtube.com/watch?v=c6PGKV0C-Ok" target="_blank" rel="noopener">click me for motivation</a>.
    </p>
    <h3>Enter the PIN Below</h3>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #ff5959;
}
</style>
