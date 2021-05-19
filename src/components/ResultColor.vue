<template>
  <ul
    :class="[code === '#FFFFFF' ? 'bg-color' : '']"
    v-if="displayResult"
    class="results-list"
  >
    <li :style="{ color: code }">
      {{ name }}
    </li>
    <li :style="{ color: code }">{{ code }}</li>
    <li :style="{ background: code }" class="color-result"></li>
  </ul>
</template>

<script>
export default {
  name: "ResultColor",
  props: {
    name: String,
    displayResult: Boolean,
    code: String,
  },
};
</script>

<style scoped>
.results-list {
  list-style-type: none;
  margin-top: 30px;
  display: flex;
  flex-direction: column;
  border: 1px solid #c5fae2;
  justify-content: space-evenly;
  margin: 30px auto;
  padding: 10px 20px;
  align-items: center;
  font-size: 18px;
}
.color-result {
  width: 50px;
  height: 50px;
  border-radius: 5px;
}
.bg-color {
  background-color: #42b983;
}
@media (min-width: 600px) {
  .results-list {
    flex-direction: row;
    width: 384px;
  }
}
</style>