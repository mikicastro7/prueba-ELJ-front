<template>
  <h2>Upload an image</h2>
  <form>
    <label className="label-img-uplader" htmlFor="img">
      <span><font-awesome-icon icon="upload" /></span>
    </label>
    <input
      class="input-img-uploader"
      id="img"
      accept="image/png,image/jpeg"
      type="file"
    />
    <button type="submit">Get result</button>
  </form>
</template>

<script>
export default {
  name: "ImgUploader",
};
</script>

<style scoped>
h2 {
  text-align: center;
}
form {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.label-img-uplader {
  margin-top: 30px;
  margin-bottom: 36px;
}
.label-img-uplader span {
  width: 100%;
  font-size: 100px;
  color: #42b883;
  text-align: center;
  cursor: pointer;
  transition: 0.5s;
  border: 2px dashed #42b883;
  display: inline-block;
  padding: 50px 40px;
  display: block;
}

.label-img-uplader span:hover {
  color: #77c8a4;
  border: 2px dashed #77c8a4;
}

.label-img-uplader {
  font-size: 24px;
}

.input-img-uploader {
  width: 0.1px;
  height: 0.1px;
  opacity: 0;
  overflow: hidden;
  position: absolute;
  z-index: -1;
}

button {
  background-color: #42b883;
  border: none;
  color: white;
  width: 200px;
  margin: auto;
  border-radius: 25px;
  font-size: 20px;
  padding: 10px 20px;
}

button:hover {
  background-color: #77c8a4;
  cursor: pointer;
}

@media (min-width: 600px) {
  .label-img-uplader span {
    font-size: 200px;
    padding: 40px 90px;
  }
}
</style>