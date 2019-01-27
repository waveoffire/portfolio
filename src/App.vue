<template>
  <div class="over" id="app">
    <div class="row menu">
      <span class="myname col-8">Piotr Smilgin</span>
      <span class="menuspan col-1">O mnie</span>
      <span class="menuspan col-1">Umiejętności</span>
      <span class="menuspan col-1">Moje projekty</span>
      <span class="menuspan col-1">Kontakt</span>
    </div>
    <div class="header">
      <div class="header-box">
        <div>Junior Front-end Developer</div>
        <div class="headername">Piotr Smilgin</div>
      </div>
    </div>
    <div
      id="about"
      class="row about"
    >Cześć, nazywam się Piotr Smilgin, a to moje portfolio. Mieszkam w Poznaniu. Pracuje jako serwisant komputerowy oraz dodatkowo, hobistycznie programuje.
      <br>Uwielbiam programować, zwłaszcza front-end. Od dłuższego czasu programuje w Vue.js.Chciałbym w przyszłości zostać programistą Front-end.
      <br>Zapraszam do obejrzenia moich projektów. Jeśli masz dla mnie propozycje współpracy - zapraszam do kontaktu.
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {};
  }
};
</script>

<style>
.menu {
  background-color: rgba(255, 255, 255, 0.6);
  padding: 15px;
  position: fixed;
  display: flex;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  color: rgb(231, 0, 0);
}
body {
  font-family: "Roboto", sans-serif;
  overflow-x: hidden;
}
.myname {
  font-size: 1.5em;
  padding-left: 10px;
}
.menuspan {
  text-align: center;
  padding-top: 5px;
}
.header {
  -webkit-clip-path: polygon(0 0, 100% 0, 100% 87vh, 0 100vh);
  clip-path: polygon(0 0, 100% 0, 100% 87vh, 0 100vh);
  z-index: 50;
  background-image: linear-gradient(
      to right bottom,
      rgba(0, 4, 255, 0.2),
      rgba(4, 235, 93, 0.4)
    ),
    url(./assets/photo/background.jpg);
  background-repeat: no-repeat;
  background-size: 100%;
  height: 100vh;
  color: white;
  text-align: center;
  font-size: 2.8em;
}
.header-box {
  top: 40%;
  left: 50%;
  transform: translate(-50%, -20%);
  position: relative;
  color: rgba(255, 255, 255, 0.8);
}
.headername {
  font-size: 2.2em;
  line-height: 0.7em;
}
.about {
  padding: 10%;
}
</style>
