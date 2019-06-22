<template>
  <div class="container" id="demo">
    <video-bg :sources="['demo/assets/scuba-diving.mp4']" img="demo/assets/fish-and-ocean.jpg">
      <div>
        <Logo/>
        <h1 class="title">We’re performing an awesome app at the moment.</h1>
        <h2 class="subtitle">So stay tuned!</h2>
      </div>
    </video-bg>
  </div>
</template>

<script src="../demo/build/build.js"></script>
<script>
import Logo from "~/components/Logo.vue";
import Vue from "vue/dist/vue.common";
import VideoBg from "../components/VideoBackground.vue";

new Vue({
  el: "#demo",
  components: { VideoBg }
});

export default {
  components: {
    Logo
  }
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 40px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 32px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.VideoBg {
  min-height: 640px;
}

.VideoBg__content {
  text-align: center;
  background-color: rgba(52, 72, 92, 0.7);
}
</style>
