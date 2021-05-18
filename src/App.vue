<template>
  <Header />
  <section class="container">
    <ImgUploader @get-color-img="getColorImg" />
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
      displayResult: false,
      colorResult: {
        colorName: "",
        colorCodeHex: "",
      },
    };
  },
  methods: {
    async getColorImg(imgFile) {
      const datos = new FormData();
      datos.append("file", imgFile);

      const res = await fetch("http://127.0.0.1:8000/api/img-most-used-color", {
        method: "POST",
        body: datos,
      });
      const data = await res.json();
      this.colorResult.colorName = data.colorName;
      this.colorResult.colorCodeHex = data.colorHex;
      if (!data.error) {
        this.displayResult = true;
      }
    },
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
