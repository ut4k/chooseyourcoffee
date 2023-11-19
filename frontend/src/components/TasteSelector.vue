<template>
  <div class="tasteSelector">
    <label for="temp">{{ title }}</label
    ><br />
    <input type="range" list="values" step="25" />
    <datalist id="values">
      <option value="0" :label="min"></option>
      <option value="25"></option>
      <option value="50"></option>
      <option value="75"></option>
      <option value="100" :label="max"></option>
    </datalist>
  </div>
</template>

<style>
.tasteSelector {
  margin: 20px 0;
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
