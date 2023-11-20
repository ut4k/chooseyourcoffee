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
        好みを選んで調整したら、「診断する！」を押してね。君好みのコーヒーを教えるよ。
      </p>
    </div>
    <div id="taste">
      <TasteSelector title="コク" min="弱い" max="強い" />
      <TasteSelector title="香り" min="弱い" max="強い" />
      <TasteSelector title="苦味" min="弱い" max="強い" />
      <TasteSelector title="酸味" min="弱い" max="強い" />
      <div>
        <button type="button">診断する！</button>
      </div>
    </div>
    <div id="result"></div>
  </main>
</template>

<style>
body {
  background: #c1c1b9;
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

#title img {
  width: 100%;
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
