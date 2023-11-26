<script setup>
import TasteSelector from "./components/TasteSelector.vue";
</script>

<template>
  <main>
    <div>
      <h1 id="title"><img src="./assets/logo.png" alt="コーヒー診断" /></h1>
    </div>
    <div>
      <p>
        好みを選んで調整したら、「診断する」を押してね。<br />君好みのコーヒーを教えるよ！
      </p>
    </div>
    <div id="taste">
      <TasteSelector title="コク" min="弱い" max="強い" />
      <TasteSelector title="香り" min="弱い" max="強い" />
      <TasteSelector title="苦味" min="弱い" max="強い" />
      <TasteSelector title="酸味" min="弱い" max="強い" />
      <div>
        <button type="button">診断する</button>
      </div>
    </div>
    <div id="result"></div>
  </main>
</template>

<style>
body {
  background-image: url('data:image/svg+xml,<svg id="visual" viewBox="0 0 960 540" width="960" height="540" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1"><rect x="0" y="0" width="960" height="540" fill="%23ffffff"></rect><defs><linearGradient id="grad1_0" x1="43.8%" y1="100%" x2="100%" y2="0%"><stop offset="14.444444444444446%" stop-color="%23ffffff" stop-opacity="1"></stop><stop offset="85.55555555555554%" stop-color="%23ffffff" stop-opacity="1"></stop></linearGradient></defs><defs><linearGradient id="grad2_0" x1="0%" y1="100%" x2="56.3%" y2="0%"><stop offset="14.444444444444446%" stop-color="%23ffffff" stop-opacity="1"></stop><stop offset="85.55555555555554%" stop-color="%23ffffff" stop-opacity="1"></stop></linearGradient></defs><g transform="translate(960, 540)"><path d="M-297 0C-250.7 -19.6 -204.4 -39.2 -188.3 -61.2C-172.2 -83.2 -186.3 -107.7 -189.3 -137.5C-192.3 -167.4 -184.1 -202.6 -166.3 -229C-148.5 -255.3 -121.1 -272.6 -91.8 -282.5C-62.4 -292.3 -31.2 -294.7 0 -297L0 0Z" fill="%23fae7ca"></path></g><g transform="translate(0, 0)"><path d="M297 0C296.1 32.1 295.1 64.2 282.5 91.8C269.8 119.4 245.4 142.5 222.5 161.6C199.6 180.8 178.3 195.9 157.5 216.8C136.8 237.7 116.7 264.3 90.5 278.7C64.4 293 32.2 295 0 297L0 0Z" fill="%23fae7ca"></path></g></svg>');
  background-repeat: no-repeat;
  background-size: cover;
  height: 100vh;
}

main {
  width: 600px;
  margin: 0 auto;
}

datalist {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  writing-mode: vertical-lr;
  width: 200px;
}

option {
  padding: 0;
}

input[type="range"] {
  width: 200px;
  margin: 0;
}

#taste {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>

<script>
export default {
  mounted() {},
  methods: {},
};
</script>
