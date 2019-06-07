<template>
  <div class="home">
    <video :src="videoFile" controls crossOrigin="anonymous"></video>
    <!-- <video ref="videoRef" src="" controls></video> -->
    <!-- S -->
  </div>
</template>

<script>
// @ is an alias to /src
import { setInterval } from 'timers';

export default {
  name: 'home',
  data(){
      return {
          params: '',
          videoFile: ''
      }
  },
  mounted(){
    this.params = this.$route.params;
    console.log(this.params);
    this.videoFile = "http://40.74.248.23:3002/download/"+this.params.videoFile;
    // console.log(this.$refs.videoRef);
    // this.$refs.videoRef.src = this.videoFile;
    // setInterval(()=> {
    //   console.log(this.$refs.videoRef.readyState);
    // }, 2000);
  }
}
</script>
