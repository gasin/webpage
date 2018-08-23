<template>
  <div>
    <h2 @mouseenter="MouseEnter" @mouseleave="MouseLeft"> Profile </h2>
    <transition name="textfade">
    <p v-if="alive === true">
      開成高校卒。<br>
      東京大学理学部情報科学科の3年生。<br>
      バイトとか課題とか趣味とかで普段はパソコンの前に座ってる人。<br>
      昔結構頑張ってたのもあって囲碁が得意。<br>
      ポーカーその他ボドゲが好き。
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
