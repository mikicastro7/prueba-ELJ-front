<template>
  <Header />
  <section class="container">
    <ImgUploader />
  </section>
</template>

<script>
import Header from "./components/Header";
import ImgUploader from "./components/ImgUploader";

export default {
  name: "App",
  components: {
    Header,
    ImgUploader,
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
