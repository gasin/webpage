<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Hobby</h2>
    <HobbyComponent />
    <h2>Organization</h2>
    <OrganizationComponent />
    <h2>Link</h2>
    <LinkComponent />
  </div>
</template>

<script>

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
    HobbyComponent: HobbyComponent,
    OrganizationComponent: OrganizationComponent,
    LinkComponent: LinkComponent
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
