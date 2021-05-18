<template>
  <Header />
  <section class="container">
    <ImgUploader />
    <ResultColor
      :displayResult="displayResult"
      :name="colorResult.colorName"
      :code="colorResult.colorCodeHex"
    />
  </section>
</template>

<script>
import Header from "./components/Header";
import ImgUploader from "./components/ImgUploader";
import ResultColor from "./components/ResultColor";

export default {
  name: "App",
  components: {
    Header,
    ImgUploader,
    ResultColor,
  },
  data() {
    return {
      displayResult: true,
      colorResult: {
        colorName: "Aqua",
        colorCodeHex: "#00FFFF",
      },
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap");
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: "Poppins", sans-serif;
}
.container {
  margin: 40px auto;
  width: 80%;
  border: 1px solid #c5fae2;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 10px 10px 10px #c5fae269;
}
</style>
