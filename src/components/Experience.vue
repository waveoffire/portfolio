<template>
  <div class="expDiv">
    <img
      class="expPhoto"
      :src="src"
      :alt="title"
    >
    <p class="expSpan">{{title}}</p>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    src: String
  }
};
</script>

<style scooped>
.expPhoto {
  height: 170px;
  max-width: 100%;
  width: auto;
  transition: all 0.15s ease-in;
}
.expPhoto:hover {
  transform: scale(1.1);
  -ms-transform: scale(1.1);
  -webkit-transform: scale(1.1);
}
.expDiv {
  display: inline-block;
  width: 200px;
  text-align: center;
  margin: 5px;
  max-width: 200px;
}
.expSpan {
  display: block;
}
</style>
