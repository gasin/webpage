<template>
  <ul id='organizations'>
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
        IS: 'https://www.is.s.u-tokyo.ac.jp/',
        TSG: 'http://www.tsg.ne.jp/'
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
  font-size: 1.5vmax;
}
a {
  color: #42b983;
}
</style>
