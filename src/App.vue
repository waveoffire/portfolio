<template>
  <div
    class="over"
    id="app"
  >
    <div id="loader-wrapper">
      <div id="loader"></div>
      <div class="loader-section section-left"></div>
      <div class="loader-section section-right"></div>
    </div>
    <div class="row menu">
      <span class="col-4">
        <span
          class="myname"
          @click="scrolling('header')"
        >Piotr Smilgin</span>
      </span>
      <div class="col-7 chamburger">
        <i
          @click="hidenned()"
          class="fa fa-bars"
          aria-hidden="true"
          style="cursor:pointer"
        ></i>
      </div>

      <span
        :class="ham"
        @click="scrolling('about')"
      >O mnie</span>
      <span
        :class="ham"
        @click="scrolling('experience')"
      >Umiejętności</span>
      <span
        :class="ham"
        @click="scrolling('projects')"
      >Moje projekty</span>
      <span
        :class="ham"
        @click="scrolling('contact')"
      >Kontakt</span>
    </div>
    <div
      id="headerstart"
      class="header"
    >
      <div class="header-box">
        <div
          data-aos="fade-left"
          data-aos-delay="1800"
        >Junior Front-end Developer</div>
        <div
          data-aos="fade-right"
          data-aos-delay="1800"
          class="headername"
        >Piotr Smilgin</div>
        <div
          class="links"
          data-aos="zoom-in"
          data-aos-delay="1800"
        >
          <a
            href="https://github.com/waveoffire"
            target="_blank"
          >
            <i
              class="fa fa-github"
              aria-hidden="true"
            ></i>
          </a>
          <a
            href="https://www.facebook.com/piotr.smilgin.7"
            target="_blank"
          >
            <i
              class="fa fa-facebook-official"
              aria-hidden="true"
            ></i>
          </a>
        </div>
      </div>
    </div>

    <div
      id="aboutstart"
      class="container-flex about"
    >
      <h1>O mnie</h1>
      <span class="line"></span>
      <div
        style="padding-top:30px;"
        class="row"
      >
        <div
          data-aos="flip-right"
          class="col-12 col-md-7 about-block"
        >Jestem Piotrek, mam 21 lat i mieszkam w Poznaniu. Szukam stałej pracy jako Front-end Developer. Najbardziej zależy mi na nauce nowych technologii i pracy z kreatywnymi i otwartymi ludźmi.
          Komputery to moja pasja a programowanie to odnaeziona po latach miłość.
          Z zawodu jestem technikiem informatykiem, a na życie zarabiam pracując w serwisie komputerowym.
        </div>
        <div class="col-md-1 col-12"></div>
        <div class="myphoto col-12 col-md-3">
          <img
            data-aos="zoom-in-left"
            src="./../public/img/myphoto.jpg"
          >
        </div>
      </div>
      <!--       <div class="row more">

        WIECEJ

      </div> -->
      <div class="row">
        <div class="col-12 col-md-3 myphoto laptop">
          <img
            data-aos="zoom-in-left"
            src="./../public/img/laptop.jpg"
          >
        </div>
        <div class="col-md-1 col-12"></div>
        <div
          class="col-12 col-md-7"
          style="padding-top:90px;"
          data-aos="flip-left"
        >
          Moim marzeniem jest podjać pracę jako Front-end Developer.
          Nie sypiam po nocach przygotowyjąc kolejne projekty.
          Dobrze czuję się w pracy w JavaScript'cie, a od jakiegoś czasu moim ulubionym frameworkiem jest Vue.js w którym pisze wiekszość swoich projektów. Wszystkie narzędzia, z których korzystam są TUTAJ.
          Przez krótki okres pracowałem w małej firmie programistycznej, więc wiem co nieco jak wygląda praca w zespole.
          Nauczyłem się tam korzystać z git'a, oraz podziału projektów na komponenty - strony są przez to bardziej wydajne i czytelne.
          W wolnym czasie poza programowaniem - Lubie też grać w gry, oglądać filmy i seriale oraz chodzić na koncerty rockowych i punkowych zespołow.
        </div>
      </div>
    </div>
    <div
      id="experiencestart"
      class="experience container-flex"
    >
      <h1>Moje umiejętności</h1>
      <span class="line"></span>
      <experience-app
        data-aos="fade-left"
        v-for="object in experiences"
        :data-aos-delay="object.time"
        :key="object.id"
        :src="object.src"
        :title="object.title"
      ></experience-app>

    </div>
    <div
      id="projectsstart"
      class="container-flex"
    >
      <h1 class=project_h1>Moje projekty</h1>
      <span class="line"></span>
      <div class="row project_row">
        <project-app
          data-aos="zoom-in"
          v-for="object in projects"
          :key="object.id"
          :photo="object.photo"
          :title="object.title"
          :github="object.github"
          :live="object.live"
        ></project-app>
      </div>
    </div>
    <div
      id="contactstart"
      class="contact"
    >
      <h2 style="text-align:center;">Kontakt</h2>
      <div
        style="padding-top:5vh"
        class="row"
      >
        <div class="col-2"></div>
        <div class=" col-11 col-sm-4">

          <i
            class="fa fa-fw fa-envelope"
            aria-hidden="true"
          ></i> Email:
          <a
            style="color:white"
            href="mailto:piotrsmilgin7@gmail.com"
          >piotrsmilgin7@gmail.com</a>

        </div>
        <div class="col-1">

        </div>
        <div class="col-11 col-sm-4">

          <i
            class="fa fa-fw fa-mobile"
            aria-hidden="true"
          ></i> Telefon: 692 943 497
        </div>
      </div>
      <div class="row">
        <div class="col-2"></div>
        <div class="col-11 col-sm-4">

          <i
            class="fa fa-fw fa-linkedin"
            aria-hidden="true"
          ></i>&nbsp;<a
            style="color:white"
            href=https://www.linkedin.com/in/piotr-smilgin-a76b94170/>LinkedIn
            </a>
            </div>
            <div
            class="col-1"
          >

        </div>
        <div class="col-11 col-sm-4">

          <i
            class="fa fa-fw fa-github"
            aria-hidden="true"
          ></i>&nbsp;<a
            style="color:white"
            href=https://github.com/waveoffire>GitHub
            </a>
            </div>
            </div>
            </div>
            </div>
            </template>

<script>
import ExperienceApp from "./components/Experience";
import ProjectApp from "./components/Project";
import AOS from "aos";
export default {
  components: {
    ExperienceApp,
    ProjectApp
  },
  name: "app",
  data() {
    return {
      experiences: [
        {
          id: 0,
          title: "HTML to podstawa każdej mojej strony",
          src: "./img/html.png",
          time: 0
        },
        {
          id: 1,
          title: "Animacje w CSS nie są mi obce",
          src: "./img/css.png",
          time: 50
        },
        {
          id: 2,
          title: "API i Front pisze w JavaScript",
          src: "./img/JavaScript.png",
          time: 100
        },
        {
          id: 3,
          title: "Vue.js to framework który skradł mi serce",
          src: "./img/vue.png",
          time: 150
        },
        {
          id: 4,
          title: "Bootstrap bez niego życie nie było by takie proste",
          src: "./img/bootstrap.png",
          time: 200
        },
        {
          id: 5,
          title: "Dane pomiedzy api-front przesyłam jako JSON",
          src: "./img/json.png",
          time: 0
        },
        {
          id: 6,
          title: "GIT to System kontroli wersji który ratuje życie",
          src: "./img/Git.png",
          time: 50
        },
        {
          id: 7,
          title: "Do swoich projektów używam również TypeScript",
          src: "./img/typescript.png",
          time: 100
        },
        {
          id: 8,
          title: "API bez Node.js by nie istniało",
          src: "./img/node.png",
          time: 150
        },
        {
          id: 9,
          title: "npm używam naprzemiennie z Yarn",
          src: "./img/npm.svg",
          time: 200
        },
        {
          id: 10,
          title: "W tym projekcie uzywam Yarn",
          src: "./img/yarn.png",
          time: 50
        }
      ],
      projects: [
        {
          id: 0,
          title:
            "Przykładowy projekt strony głownej w vanilla javascript i css",
          photo: "./img/homepage.png",
          github: "https://github.com/waveoffire/HomePage",
          live: "https://waveoffire.github.io/HomePage/"
        },
        {
          id: 1,
          title:
            "Projekt w trakcie realizacji z użyciem Vue.js, pokazujący ciekawe oferty oraz zmiany w cenach samochodów",
          photo: "./img/zdzis.png",
          live: "http://pb.zdzis.com/home"
        },
        {
          id: 2,
          title: "Strona na którą właśnie patrzysz - napisana w Vue.js",
          photo: "./img/portfolio.png",
          github: "https://github.com/waveoffire/portfolio",
          live: "https://waveoffire.github.io/portfolio/"
        }
      ],
      ham: "menuspan hiddenbox col-sm-2"
    };
  },
  methods: {
    scrolling(nazwa) {
      document.querySelector("#" + nazwa + "start").scrollIntoView({
        behavior: "smooth",

        block: "center",
        inline: "start"
      });
    },
    hidenned() {
      if (this.ham != "menuspan col-sm-2 hidden") {
        this.ham = "menuspan col-sm-2 hidden";
      } else {
        this.ham = "menuspan hiddenbox col-sm-2";
      }
    }
  },
  mounted() {
    let element = document.getElementsByTagName("body");
    setTimeout(function() {
      element[0].classList.add("loaded");
    }, 1500);
  }
};
</script>

<style>
.more {
  left: 0;
  background-image: linear-gradient(
    to bottom,
    rgba(44, 44, 44, 0.651),
    rgba(32, 32, 32, 0.425)
  );
  -webkit-clip-path: polygon(0 10%, 100% 0, 80% 100%, 0 100%);
  clip-path: polygon(0 0, 100% 0, 80% 100%, 0 100%);

  background-size: 100%;
}
#loader-wrapper {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1000;
}
#loader {
  display: block;
  position: relative;
  left: 50%;
  top: 50%;
  width: 150px;
  height: 150px;
  z-index: 1001;
  margin: -75px 0 0 -75px;
  border-radius: 50%;
  border: 3px solid transparent;
  border-top-color: #3498db;
  -webkit-animation: spin 2s linear infinite; /* Chrome, Opera 15+, Safari 5+ */
  animation: spin 2s linear infinite; /* Chrome, Firefox 16+, IE 10+, Opera */
}

#loader:before {
  content: "";
  position: absolute;
  top: 5px;
  left: 5px;
  right: 5px;
  bottom: 5px;
  border-radius: 50%;
  border: 3px solid transparent;
  border-top-color: #5ee73c;
  -webkit-animation: spin 3s linear infinite; /* Chrome, Opera 15+, Safari 5+ */
  animation: spin 3s linear infinite; /* Chrome, Firefox 16+, IE 10+, Opera */
}

#loader:after {
  content: "";
  position: absolute;
  top: 15px;
  left: 15px;
  right: 15px;
  bottom: 15px;
  border-radius: 50%;
  border: 3px solid transparent;
  border-top-color: #fafafa;
  -webkit-animation: spin 1.5s linear infinite; /* Chrome, Opera 15+, Safari 5+ */
  animation: spin 1.5s linear infinite; /* Chrome, Firefox 16+, IE 10+, Opera */
}

@-webkit-keyframes spin {
  0% {
    -webkit-transform: rotate(0deg); /* Chrome, Opera 15+, Safari 3.1+ */
    -ms-transform: rotate(0deg); /* IE 9 */
    transform: rotate(0deg); /* Firefox 16+, IE 10+, Opera */
  }
  100% {
    -webkit-transform: rotate(360deg); /* Chrome, Opera 15+, Safari 3.1+ */
    -ms-transform: rotate(360deg); /* IE 9 */
    transform: rotate(360deg); /* Firefox 16+, IE 10+, Opera */
  }
}
@keyframes spin {
  0% {
    -webkit-transform: rotate(0deg); /* Chrome, Opera 15+, Safari 3.1+ */
    -ms-transform: rotate(0deg); /* IE 9 */
    transform: rotate(0deg); /* Firefox 16+, IE 10+, Opera */
  }
  100% {
    -webkit-transform: rotate(360deg); /* Chrome, Opera 15+, Safari 3.1+ */
    -ms-transform: rotate(360deg); /* IE 9 */
    transform: rotate(360deg); /* Firefox 16+, IE 10+, Opera */
  }
}
#loader-wrapper .loader-section {
  position: fixed;
  top: 0;
  width: 55.7%;
  height: 100%;

  z-index: 1000;
}

#loader-wrapper .loader-section.section-left {
  left: 0;
  background-image: linear-gradient(
      to bottom,
      rgba(44, 44, 44, 0.651),
      rgba(32, 32, 32, 0.425)
    ),
    url(./../public/img/dots.jpg);
  -webkit-clip-path: polygon(0 0, 100% 0, 80% 100%, 0 100%);
  clip-path: polygon(0 0, 100% 0, 80% 100%, 0 100%);

  background-size: 100%;
}

#loader-wrapper .loader-section.section-right {
  right: 0;
  background-image: linear-gradient(
      to bottom,
      rgba(44, 44, 44, 0.651),
      rgba(32, 32, 32, 0.425)
    ),
    url(./../public/img/dots.jpg);
  background-size: 100%;
  clip-path: polygon(20% 0, 100% 0, 100% 100%, 0 100%);
}
.loaded #loader-wrapper .loader-section.section-left {
  -webkit-transform: translateX(-100%); /* Chrome, Opera 15+, Safari 3.1+ */
  -ms-transform: translateX(-100%); /* IE 9 */
  transform: translateX(-100%); /* Firefox 16+, IE 10+, Opera */
}

.loaded #loader-wrapper .loader-section.section-right {
  -webkit-transform: translateX(100%); /* Chrome, Opera 15+, Safari 3.1+ */
  -ms-transform: translateX(100%); /* IE 9 */
  transform: translateX(100%); /* Firefox 16+, IE 10+, Opera */
}
.loaded #loader {
  opacity: 0;
  -webkit-transition: all 0.3s ease-out;
  transition: all 0.3s ease-out;
}
.loaded #loader-wrapper {
  visibility: hidden;
}
.loaded #loader-wrapper .loader-section.section-right,
.loaded #loader-wrapper .loader-section.section-left {
  -webkit-transition: all 0.3s 0.3s cubic-bezier(0.645, 0.045, 0.355, 1);
  transition: all 0.3s 0.3s cubic-bezier(0.645, 0.045, 0.355, 1);
}
.loaded #loader-wrapper {
  -webkit-transform: translateY(-100%);
  -ms-transform: translateY(-100%);
  transform: translateY(-100%);

  -webkit-transition: all 0.3s 1s ease-out;
  transition: all 0.3s 1s ease-out;
}
.no-js #loader-wrapper {
  display: none;
}
.line {
  width: 100px;
  height: 1px;
  border: 2px solid rgb(0, 204, 255);
  display: block;
  margin: auto;
  transform: translateY(-30px);
}
.experience .line {
  width: 200px;
  transform: translateY(-50px);
}
#projectsstart .line {
  width: 150px;
}
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
  cursor: pointer;
}
.project_row {
  padding-top: 100px;
}
.menuspan {
  text-align: center;
  padding-top: 5px;
  cursor: pointer;
  font-size: 1.3em;
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
    url(./../public/img/background.jpg);
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
.about-block {
  padding-top: 70px;
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
  width: 100%;
  font-size: 1.4em;
}

.myphoto {
  display: inline-block;
  width: 40%;
}

.hidden {
  display: block;
}

.myphoto img {
  width: 100%;
  border-radius: 50%;
  transform: translateX(10%);
}
.laptop img {
  width: 400px;
  height: 400px;
}
.contact {
  -webkit-clip-path: polygon(0 13vh, 100% 0, 100% 50vh, 0 50vh);
  clip-path: polygon(0 13vh, 100% 0, 100% 50vh, 0 50vh);
  z-index: 50;
  background-image: linear-gradient(to bottom, #002d47, #001927);
  background-repeat: no-repeat;
  background-size: 100%;
  padding-top: 13vh;
  height: 50vh;
  color: white;
  font-size: 2em;
}

.experience h1 {
  padding-bottom: 50px;
  padding-top: 50px;
}

.chamburger {
  display: none;
}

.npm {
  width: auto;
  display: inline-block;
  text-align: center;

  max-width: 100%;
}

.links i {
  margin: 10px;
  cursor: pointer;
}

.links a {
  color: rgba(255, 255, 255, 0.8);
}

.links a:hover {
  color: rgba(255, 255, 255, 1);
}

.hiddenbox {
  display: block;
}

.chamburger {
  text-align: right;
  padding: 5px;
}
.container-flex {
  padding: 5vh 20vh 5vh 20vh;
}
.experience {
  text-align: center;
  padding: 0 35vh 5vh 35vh;
  margin-top: 5vh;

  background-size: 100%;
  background-image: linear-gradient(to bottom right, #008300a6, #0091aaa8),
    url(./../public/img/paper.jpg);
}
.project_h1 {
  padding-top: 200px;
}
@media only screen and (max-width: 1000px) {
  .myphoto {
    width: 100%;
  }
  .container-flex {
    padding: 5vh 5vh 5vh 5vh;
  }
  .laptop {
    width: 100%;
  }
  .laptop img {
    width: 100%;
    height: auto;
    padding-top: 15px;
  }
  .myphoto img {
    transform: translateX(0%);
  }
  .about {
    width: 100%;
    font-size: 1.1rem;
    padding-top: 0px;
  }
  h1 {
    padding-top: 100px;
  }
  .header {
    background-size: 150%;
    font-size: 2em;
  }
  .menuspan {
    font-size: 1em;
  }
  .contact {
    font-size: 1.2em;
    overflow: hidden;
  }

  .experience {
    padding: 0 5vh 5vh 5vh;
  }
  .about-block {
    padding-top: 0;
  }
  .project_row {
    padding-top: 20px;
  }
}

@media only screen and (max-width: 600px) {
  .header {
    background-size: 250%;
    font-size: 1.5em;
  }
  .chamburger {
    display: block;
  }
  .hiddenbox {
    display: none;
  }
  .myname {
    font-size: 1.3rem;
  }
  .contact {
    font-size: 1em;
  }
  .experience h1 {
    font-size: 1.5em;
  }
  .container-flex h1 {
    font-size: 1.5em;
    padding-top: 40px;
  }
}
</style>
