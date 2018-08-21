<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li>
        <a
          href="https://twitter.com/_gacin"
          target="_blank"
        >
          Twitter
        </a>
      </li>
      <li>
        <a
          href="http://gasin.hatenadiary.jp/"
          target="_blank"
        >
          Blog
        </a>
      </li>
      <li>
        <a
          href="https://github.com/gasin"
          target="_blank"
        >
          Github
        </a>
      </li>
    </ul>
    <h2>Organization Links</h2>
    <ul>
      <li>
        <a
          href="https://www.is.s.u-tokyo.ac.jp/"
          target="_blank"
        >
          IS
        </a>
      </li>
      <li>
        <a
          href="http://www.tsg.ne.jp/"
          target="_blank"
        >
          TSG
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to gasin\'s room'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
  color: #42b983;
}
</style>
