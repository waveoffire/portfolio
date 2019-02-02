<template>
  <div class="expDiv">
    <img class="expPhoto" :src="src" alt="CSS">
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
  height: 150px;
  max-width: 100%;
}
.expDiv {
  display: inline-block;
  width: 200px;
  text-align: center;
  margin: 5px;
}
.expSpan {
  display: block;
}
</style>
