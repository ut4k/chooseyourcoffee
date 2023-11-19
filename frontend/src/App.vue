<script setup>
import TasteSelector from "./components/TasteSelector.vue";
</script>

<template>
  <main>
    <div>
      <h1>コーヒー診断</h1>
    </div>
    <div>
      <p>
        好みを選んで調整したら、「診断する！」を押してね。君好みのコーヒーを教えるよ。
      </p>
    </div>
    <div>
      <TasteSelector title="コク" min="弱い" max="強い" />
      <TasteSelector title="香り" min="弱い" max="強い" />
      <TasteSelector title="苦味" min="弱い" max="強い" />
      <TasteSelector title="酸味" min="弱い" max="強い" />
    </div>
    <div>
      <button type="button">診断する！</button>
    </div>
    <div id="result"></div>
  </main>
</template>

<style>
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
</style>

<script>
export default {
  mounted() {},
  methods: {},
};
</script>
