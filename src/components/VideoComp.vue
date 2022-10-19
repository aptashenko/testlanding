<template>
    <video ref="player" class="videoPlayer" muted="muted" playsinline>
        Sorry, your browser doesn't support this video
    </video>
</template>

<script>
var throttle = require('lodash.throttle');
export default {
    data() {
        return {
            savedTime: localStorage.getItem('video-time'),
        }
    },
    methods: {
        startVideo() {
            const video = this.$refs.player;
            video.src = require('../assets/video/timer.mp4');
            this.savedTime ? video.currentTime = this.savedTime : video.currentTime = 0;
            video.loop = true;
            video.play();
            video.addEventListener('timeupdate', throttle(() => {
                localStorage.setItem('video-time', JSON.stringify(video.currentTime))
            }, 1000))
        }
    },
    mounted() {
        this.startVideo();
    },
}
</script>

<style lang="scss">
.videoPlayer {
      max-width: 100%;
      margin: 32px auto;
      display: block;
      border: 2px solid #fff;
  }
</style>