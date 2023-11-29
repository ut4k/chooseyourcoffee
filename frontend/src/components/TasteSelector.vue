<template>
  <div class="tasteSelector">
    <div class="flex-container">
      <label class="taste-label" for="temp">{{ title }}</label>
      <input type="range" list="values" step="25" />
    </div>
    <div class="flex-container">
      <label class="taste-label invis">{{ title }}</label>
      <datalist id="values">
        <option value="0" :label="min"></option>
        <option value="25"></option>
        <option value="50"></option>
        <option value="75"></option>
        <option value="100" :label="max"></option>
      </datalist>
    </div>
  </div>
</template>

<style>
.tasteSelector {
  margin: 20px 72px 0 0;
}
</style>

<script>
export default {
  props: {
    title: String,
    min: String,
    max: String,
  },
};
</script>
