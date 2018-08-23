<template>
  <div>
    <h2 @mouseenter="MouseEnter" @mouseleave="MouseLeft"> Career </h2>
    <transition name="textfade">
    <p v-if="alive === true">
      元日本棋院院生。<br>
      高校囲碁選手権個人準優勝、団体優勝など。<br>
      JOI春合宿参加。<br>
      Unipro Inc.での1年半のアルバイト経験。<br>
    </p>
    </transition>
  </div>
</template>

<script>

export default {
  data: function () {
    return {
      alive: false
    }
  },
  methods: {
    MouseEnter: function () {
      this.alive = true
    },
    MouseLeft: function () {
      this.alive = false
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
p {
    position: absolute;
    transform: translate(-50%);
    display: inline-block;
    font-weight: normal;
    color: #55ffff;
    font-size: 1.3vmax;
    border: double medium black;
    border-radius: 10px;
    background-color: #333333;

    padding-left: 10px;
    text-align: left;
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

.textfade-enter-active, .textfade-leave-active {
  transition: opacity 1s;
}
.textfade-enter, .textfade-leave-to {
  opacity: 0;
}
</style>
