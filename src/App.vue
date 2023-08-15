<!-- <script setup>
import HelloWorld from './components/HelloWorld.vue';
import Niivue from './components/Niivue.vue';

</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="BrainZ" />
  <Niivue />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>

 -->

<script>
import {Niivue} from '@niivue/niivue'
const nv = new Niivue()


export default {
  name: 'App',
  props: {

  },
  data(){
    return {
      volumeList: [
        {
          url: "https://niivue.github.io/niivue-demo-images/mni152.nii.gz",
        }
      ]

    }
  },

  mounted() {

    nv.attachTo('gl')
    nv.loadVolumes(this.volumeList)
  }
}

</script>

<template>
<canvas id="gl" height="480" width="640">

</canvas>
</template>
