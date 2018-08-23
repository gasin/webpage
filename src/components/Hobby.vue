<template>
  <div>
  <h2>Hobby</h2>
  <ul id='hobbies'>
    <li v-for="title in titles" :key=title>
      {{title}}
    </li>
  </ul>
  </div>
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
h1 {
  font-weight: normal;
}
h2 {
  text-align: left;
  color: #ffffff;
  font-size: 2vmax;

  animation-name: subtitle-up-anime;
  animation-duration: 10s;
  animation-timing-function: ease;
  animation-iteration-count: 1;
  animation-delay: 0s;

  transition: all 2s;
}
@keyframes subtitle-up-anime {
  0% {
    margin: 100vh auto 0;
    transform: translateY(-50%);
  }
  60% {
    margin: 100vh auto 0;
    transform: translateY(-50%);
  }
  100% {
  }
}
h2:hover {
  background-image: linear-gradient(90deg, #ffffff, #333333);
  color: #000000;
  padding-left: 30%;
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
