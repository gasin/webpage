<template>
  <div>
  <h2> Organization </h2>
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
  </div>
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
  margin: 0 10px;
  background: #793d0c;

  border-radius: 5px;
  border: solid thin black;
}
a {
  padding: 0px 5px;
  text-decoration: none;
  font-size: 1.5vmax;
  color: gray;

  transition: all 1s;
}
a:hover {
    opacity: 0.5;
    font-size: 2.0vmax;
}
</style>
