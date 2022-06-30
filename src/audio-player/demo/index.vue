<template>
  <demo-section>
    <demo-block title="基础用法">
      <audio-player @ready="handleReady" />
    </demo-block>
  </demo-section>
</template>

<script>
import AudioPlayer from '../index.vue';

export default {
  components: {
    AudioPlayer,
  },
  data() {
    return {};
  },
  methods: {
    handleReady(player) {
      player.load('https://static.refined-x.com/static/sample.mp3');
    },
    handleHeartbeat(time) {
      console.log('time==', time);
    },
  },
};
</script>
