<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <ProfileComponent />
    <h2>Hobby</h2>
    <HobbyComponent />
    <h2>Organization</h2>
    <OrganizationComponent />
    <h2>Link</h2>
    <LinkComponent />
  </div>
</template>

<script>

import ProfileComponent from './Profile.vue'
import HobbyComponent from './Hobby.vue'
import OrganizationComponent from './Organization.vue'
import LinkComponent from './Link.vue'

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'gasin\'s room'
    }
  },
  components: {
    ProfileComponent: ProfileComponent,
    HobbyComponent: HobbyComponent,
    OrganizationComponent: OrganizationComponent,
    LinkComponent: LinkComponent
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: normal;
  color: #ffffff;
  font-size: 5vmax;
  font-family: 'Shadows Into Light', cursive;

  animation-name: title-up-anime;
  animation-duration: 6s;
  animation-timing-function: ease;
  animation-iteration-count: 1;
  animation-delay: 0s;
}
@keyframes title-up-anime {
  0% {
    margin: 50vh auto 0;
    transform: translateY(-50%);
    font-size: 0%;
  }
  40% {
    margin: 50vh auto 0;
    transform: translateY(-50%);
    font-size: 16vmax;
  }
  50% {
    margin: 50vh auto 0;
    transform: translateY(-50%);
    font-size: 8vmax;
  }
  100% {
  }
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
