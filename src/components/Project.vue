<template>
  <div class="col-12 col-md-6 projectdiv">
    <img class="projectphoto" :src="photo">
    <div class="projecthover">
      <span>
        {{title}}
        <br>
        <br>

        <a v-if="github" :href="github" class="btn btn-outline-light">GITHUB</a>
        
        <a v-if="live" :href="live" class="btn btn-outline-light">LIVE</a>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    photo: String,
    github: String,
    live: String
  }
};
</script>

<style scooped>
.projectdiv {
  width: 50%;
  position: relative;
  padding: 10px;
}
.projectphoto {
  width: 100%;
  border-radius: 10px;
}
.projecthover {
  opacity: 0;
  margin: 10px 10px 10px 10px;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  color: white;
  background-image: linear-gradient(
    to right bottom,
    rgba(0, 4, 255, 0.4),
    rgba(4, 235, 93, 0.6)
  );
  text-align: center;
  border-radius: 10px;
}
.projecthover span {
  top: 30%;
  width: 100%;
  padding: 15px;
  position: relative;
}
.projecthover:hover {
  opacity: 1;
}
.projecthover a {
  margin: 5px;
}
</style>
