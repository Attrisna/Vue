<template>
  <div id="app" ref="body">
    <nav-bar></nav-bar>

    <main class="main">
      <video
        src="@/assets/img/video.mp4"
        autoplay
        loop
        muted
        type="mp4"
      ></video>
      <img src="@/assets/img/wrapper.jpg" class="wrapper" alt="" />
      <h2>One Piece</h2>

      <p class="copyright">Copyright © 2023 MAM</p>
      <ul class="sosmed">
        <li>
          <a href="#"><i class="fas fa-twitter"></i></a>
        </li>
        <li>
          <a href="#"><i class="fas fa-github"></i></a>
        </li>
        <li>
          <a href="#"><i class="fas fa-instagram"></i></a>
        </li>
      </ul>
    </main>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {
    NavBar: () => import("@/components/NavBar.vue"),
  },
  mounted() {
    this.$store.state.body = this.$refs.body;
  },
};
</script>

<style lang="scss">
@import "@/assets/css/app.scss";
</style>
