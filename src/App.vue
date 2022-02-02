<template>
  <navigation></navigation>
  <div class="grid place-items-center h-screen shadow-2xl rounded-md">
    <div id="twitch-embed"></div>
  </div>
</template>

<script>
import Navigation from "./components/Navigation.vue";
export default {
  components: {
    Navigation,
  },
  mounted() {
    const options = {
      width: "854",
      height: "480",
      channel: "wartnerio",
      layout: "video",
      autoplay: true,
      muted: true,
      theme: "light",
    };
    const player = new Twitch.Player("twitch-embed", options);
    player.setVolume(0.5);
    player.play();
  },
};
</script>

<style>
</style>
