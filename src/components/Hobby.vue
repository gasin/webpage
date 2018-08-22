<template>
  <ul id='hobbies'>
    <li v-for="title in titles" :key=title>
      {{title}}
    </li>
  </ul>
</template>

<script>

export default {
  data () {
    return {
      titles: ['Programming', 'Go']
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
  padding: 0 10px;
  font-size: 1.5vmax;
  color: #42b983;
}
a {
  color: #42b983;
}
</style>
