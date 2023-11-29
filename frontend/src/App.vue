<script setup>
import TasteSelector from "./components/TasteSelector.vue";
</script>

<template>
  <main>
    <div>
      <h1 id="title"><img src="./assets/logo.png" alt="コーヒー診断" /></h1>
    </div>
    <div>
      <p class="text-medium">
        好みを選んだら、「診断する」を押してね。<br />君好みのコーヒーを教えるよ！
      </p>
    </div>
    <div id="taste">
      <TasteSelector title="コク" min="弱い" max="強い" />
      <TasteSelector title="香り" min="弱い" max="強い" />
      <TasteSelector title="苦味" min="弱い" max="強い" />
      <TasteSelector title="酸味" min="弱い" max="強い" />
      <div id="taste-confirm">
        <button class="my-button" type="button">診断する</button>
      </div>
    </div>
    <div id="result"></div>
  </main>
</template>

<style>
* {
  font-family: "Murecho", sans-serif;
}

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
  width: 18.5rem;
}

option {
  padding: 0;
}

/*********** Baseline, reset styles ***********/
input[type="range"] {
  -webkit-appearance: none;
  appearance: none;
  background: transparent;
  cursor: pointer;
  width: 100%;
}

/* Removes default focus */
input[type="range"]:focus {
  outline: none;
}

/******** Chrome, Safari, Opera and Edge Chromium styles ********/
/* slider track */
input[type="range"]::-webkit-slider-runnable-track {
  background-color: #ffdbb3;
  border-radius: 0rem;
  height: 0.5rem;
}

/* slider thumb */
input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none; /* Override default look */
  appearance: none;
  background-color: #9e5829;
  border-radius: 0rem;
  margin-top: -12px;
  height: 40px;
  width: 34px;
  background: url("./assets/coffee-bean.png") no-repeat 0 0;
}

/*********** Firefox styles ***********/
/* slider track */
input[type="range"]::-moz-range-track {
  background-color: #ffdbb3;
  border-radius: 0rem;
  height: 0.5rem;
}

/* slider thumb */
input[type="range"]::-moz-range-thumb {
  background-color: #9e5829;
  border: none; /*Removes extra border that FF applies*/
  border-radius: 0rem;
  margin-top: -12px;
  height: 40px;
  width: 34px;
  background: url("./assets/coffee-bean.png") no-repeat 0 0;
}

#taste {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

#taste-confirm {
  margin-top: 20px;
}

.taste-label {
  white-space: nowrap;
  font-size: 1.5rem;
  padding: 0 1rem;
}

.my-button {
  box-shadow: inset 0px 1px 0px 0px #a6827e;
  background-color: #7d5d3b;
  border-radius: 3px;
  border: 1px solid #54381e;
  display: inline-block;
  cursor: pointer;
  color: #ffffff;
  font-family: Arial;
  font-size: 26px;
  padding: 16px 34px;
  text-decoration: none;
  text-shadow: 0px 1px 0px #4d3534;
}
.my-button:hover {
  background-color: #634b30;
}
.my-button:active {
  position: relative;
  top: 1px;
}

.text-medium {
  font-size: 1.3rem;
}

.flex-container {
  display: flex;
}

.invis {
  visibility: hidden;
}

@import url("https://fonts.googleapis.com/css2?family=Murecho&display=swap");
</style>

<script>
export default {
  mounted() {},
  methods: {},
};
</script>
