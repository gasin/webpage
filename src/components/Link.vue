<template>
  <ul id='links'>
    <li v-for="(title,url) in links" :key=title>
      <a
        :href=title
        target="_blank"
      >
        {{url}}
      </a>
    </li>
  </ul>
</template>

<script>

export default {
  data () {
    return {
      links: {
        Twitter: 'https://twitter.com/_gacin',
        Blog: 'http://gasin.hatenadiary.jp/',
        Github: 'https://github.com/gasin'
      }
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
