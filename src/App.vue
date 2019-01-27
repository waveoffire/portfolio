<template>
  <div class="over" id="app">
    <div class="row menu">
      <span class="myname col-8" @click="scrolling('header')">Piotr Smilgin</span>
      <span class="menuspan col-1" @click="scrolling('about')">O mnie</span>
      <span class="menuspan col-1" @click="scrolling('experience')">Umiejętności</span>
      <span class="menuspan col-1" @click="scrolling('projects')">Moje projekty</span>
      <span class="menuspan col-1" @click="scrolling('contact')">Kontakt</span>
    </div>
    <div id="headerstart" class="header">
      <div class="header-box">
        <div>Junior Front-end Developer</div>
        <div class="headername">Piotr Smilgin</div>
        <div class="links">
          <a href="https://github.com/waveoffire" target="_blank">
            <i class="fa fa-github" aria-hidden="true"></i>
          </a>
          <a href="https://www.facebook.com/piotr.smilgin.7" target="_blank">
            <i class="fa fa-facebook-official" aria-hidden="true"></i>
          </a>
        </div>
      </div>
    </div>
    <div id="aboutstart" class="container">
      <h1>O mnie</h1>
      <div style="padding-top:100px;" class="row">
        <div
          class="col-7 about"
        >Cześć, nazywam się Piotr Smilgin, a to moje portfolio. Mieszkam w Poznaniu. Pracuje jako serwisant komputerowy oraz dodatkowo, hobistycznie programuje.
          <br>Uwielbiam programować, zwłaszcza front-end. Od dłuższego czasu programuje w Vue.js. Chciałbym w przyszłości zostać programistą Front-end.
          <br>Zapraszam do obejrzenia moich projektów. Jeśli masz dla mnie propozycje współpracy - zapraszam do kontaktu.
        </div>
        <div class="myphoto col-5">
          <img src="./assets/photo/myphoto.jpg">
        </div>
      </div>
    </div>
    <div id="experiencestart" class="experience container">
      <h1>Moje umiejętności</h1>
      <div class="expDiv">
        <img class="expPhoto" src="./assets/photo/html.png" alt="HTML">

        <p class="expSpan">HTML to podstawa każdej mojej strony</p>
      </div>
      <div class="expDiv">
        <img class="expPhoto" src="./assets/photo/css.png" alt="CSS">
        <p class="expSpan">Animacje w CSS nie są mi obce</p>
      </div>
      <div class="expDiv">
        <img class="expPhoto" src="./assets/photo/JavaScript.png" alt="JAVASCRIPT">
        <span class="expSpan">API i Front pisze w JavaScript</span>
      </div>
      <div class="expDiv">
        <img class="expPhoto" src="./assets/photo/vue.png" alt="VUE.JS">
        <span class="expSpan">Vue.js to framework który skradł mi serce</span>
      </div>
      <div class="expDiv">
        <img class="expPhoto" src="./assets/photo/bootstrap.png" alt="BOOTSTRAP">
        <span class="expSpan">Bootstrap bez niego życie nie było by takie proste</span>
      </div>
      <div class="expDiv">
        <img class="expPhoto" src="./assets/photo/json.png" alt="JSON">
        <span class="expSpan">Dane pomiedzy api-front przesyłam jako JSON</span>
      </div>
      <div class="expDiv">
        <img class="expPhoto" src="./assets/photo/Git.png" alt="GIT">
        <span class="expSpan">GIT to System kontroli wersji który ratuje życie</span>
      </div>
      <div class="expDiv">
        <img class="expPhoto" src="./assets/photo/typescript.png" alt="TYPESCRIPT">
        <span class="expSpan">Do swoich projektów używam również TypeScript</span>
      </div>
      <div class="expDiv">
        <img class="expPhoto" src="./assets/photo/node.png" alt="NODE">
        <span class="expSpan">API bez Node.js by nie istniało</span>
      </div>
      <div>
        <div class="expDiv npm">
          <img class="expPhoto" src="./assets/photo/npm.svg" alt="NPM">
        </div>
        <div class="expDiv npm">
          <img class="expPhoto" src="./assets/photo/yarn.png" alt="YARN">
        </div>
        <!--  <img class="expPhoto" src="./assets/photo/mysql.png" alt="MYSQL"> -->
      </div>
      <span class="expSpan">NPM i Yarn używam naprzemiennie</span>
    </div>
    <div id="projectsstart" class="container">
      <h1>Moje projekty</h1>
      <div style="padding-top:100px;" class="row">
        <div class="col-6 projectdiv">
          <img class="projectphoto" src="./assets/photo/homepage.png">
          <div class="projecthover">
            <span>
              Przykładowy projekt strony głownej w vanilla javascript i css
              <br>
              <br>
              <button class="btn btn-outline-light">GITHUB</button>
              <button class="btn btn-outline-light">LIVE</button>
            </span>
          </div>
        </div>
        <div class="col-6 projectdiv">
          <img class="projectphoto" src="./assets/photo/zdzis.png">
          <div class="projecthover">
            <span>Projekt w trakcie realizacji z użyciem Vue.js, pokazujący ciekawe oferty oraz zmiany w cenach samochodów
              <br>
              <br>

              <button class="btn btn-outline-light">LIVE</button>
            </span>
          </div>
        </div>
      </div>
    </div>
    <div id="contactstart" class="contact"></div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {};
  },
  methods: {
    scrolling(nazwa) {
      document.querySelector("#" + nazwa + "start").scrollIntoView({
        behavior: "smooth",
        alignTo: "False"
      });
    }
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
  border-bottom: 1px solid rgba(128, 128, 128, 0.473);
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
h1 {
  padding: 30px;
  text-align: center;
  padding-top: 150px;
}
.about {
  display: inline-block;
  width: 60%;
  font-size: 1.4em;
  padding-top: 90px;
  height: 80vh;
}
.myphoto {
  display: inline-block;
  width: 40%;
}
.myphoto img {
  width: 100%;
  border-radius: 50%;
  transform: translateX(10%);
}
.contact {
  -webkit-clip-path: polygon(0 13vh, 100% 0, 100% 50vh, 0 50vh);
  clip-path: polygon(0 13vh, 100% 0, 100% 50vh, 0 50vh);
  z-index: 50;
  background-image: linear-gradient(to bottom, #002d47, #001927);
  background-repeat: no-repeat;
  background-size: 100%;

  height: 50vh;
  color: white;
  text-align: center;
  font-size: 2.8em;
}
.experience {
  text-align: center;
}
.experience h1 {
  padding-bottom: 100px;
  padding-top: 20px;
}
.expPhoto {
  height: 150px;
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
.npm {
  width: 400px;
}
.links i {
  margin: 10px;
  cursor: pointer;
}
a {
  color: rgba(255, 255, 255, 0.8);
}
a:hover {
  color: rgba(255, 255, 255, 1);
}
.projectdiv {
  width: 50%;
  position: relative;
  padding: 0 10px 0 10px;
}
.projectphoto {
  width: 100%;
  border-radius: 10px;
}
.projecthover {
  opacity: 0;
  margin: 0 10px 0 10px;
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
</style>
