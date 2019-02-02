<template>
  <div class="over" id="app">
    <div class="row menu">
      <span class="col-4">
        <span class="myname" @click="scrolling('header')">Piotr Smilgin</span>
      </span>
      <div class="col-7 chamburger">
        <i @click="hidenned()" class="fa fa-bars" aria-hidden="true" style="cursor:pointer"></i>
      </div>

      <span :class="ham" @click="scrolling('about')">O mnie</span>
      <span :class="ham" @click="scrolling('experience')">Umiejętności</span>
      <span :class="ham" @click="scrolling('projects')">Moje projekty</span>
      <span :class="ham" @click="scrolling('contact')">Kontakt</span>
    </div>
    <div id="headerstart" class="header">
      <div class="header-box">
        <div data-aos="fade-left">Junior Front-end Developer</div>
        <div data-aos="fade-right" class="headername">Piotr Smilgin</div>
        <div class="links" data-aos="zoom-in">
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
          data-aos="flip-right"
          class="col-12 col-md-7 about"
        >Cześć, nazywam się Piotr Smilgin, a to moje portfolio. Mieszkam w Poznaniu. Pracuje jako serwisant komputerowy oraz dodatkowo, hobistycznie programuje.
          <br>Uwielbiam programować, zwłaszcza front-end. Od dłuższego czasu programuje w Vue.js. Chciałbym w przyszłości zostać programistą Front-end.
          <br>Zapraszam do obejrzenia moich projektów. Jeśli masz dla mnie propozycje współpracy - zapraszam do kontaktu.
        </div>
        <div class="myphoto col-12 col-md-5">
          <img data-aos="zoom-in-left" src="./../public/img/myphoto.jpg">
        </div>
      </div>
    </div>
    <div id="experiencestart" class="experience container">
      <h1>Moje umiejętności</h1>
      <experience-app
        data-aos="fade-left"
        :data-aos-delay="object.id*100"
        v-for="object in experiences"
        :key="object.id"
        :src="object.src"
        :title="object.title"
      ></experience-app>
      <div data-aos="fade-up" data-aos-delay="200">
        <div class="expDiv npm">
          <img class="expPhoto" src="./../public/img/npm.svg" alt="NPM">
        </div>
        <div class="expDiv npm">
          <img class="expPhoto" src="./../public/img/yarn.png" alt="YARN">
        </div>
        <!--  <img class="expPhoto" src="./assets/photo/mysql.png" alt="MYSQL"> -->
        <span class="expSpan">NPM i Yarn używam naprzemiennie</span>
      </div>
    </div>
    <div id="projectsstart" class="container">
      <h1 style="padding-top:200px">Moje projekty</h1>
      <div style="padding-top:100px;" class="row">
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
    <div id="contactstart" class="contact">
      <h2 style="text-align:center;">Kontakt</h2>    <div class="row">
        <div class="col-2"></div>
        <div class=" col-4 col-sm-12">

      <i class="fa fa-fw fa-envelope" aria-hidden="true"></i>
  

      Email:
      <a
        style="color:white"
        href="mailto:piotrsmilgin7@gmail.com"
      >piotrsmilgin7@gmail.com</a>
      
        </div>
        <div class="col-1">

        </div>
        <div class="col-4 col-sm-12">

      <i class="fa fa-fw fa-mobile" aria-hidden="true"></i> Telefon: 692 943 497
        </div>
      </div>
      <div class="row">
        <div class="col-2"></div>
<div class="col-4 col-sm-12">

      <i class="fa fa-fw fa-linkedin" aria-hidden="true"></i>&nbsp;<a  style="color:white" href=https://www.linkedin.com/in/piotr-smilgin-a76b94170/>LinkedIn</a>
</div>        <div class="col-1">
          
        </div><div class="col-4 col-sm-12">

      <i
        class="fa fa-fw fa-github"
        aria-hidden="true"
      ></i>&nbsp;<a style="color:white" href=https://github.com/waveoffire>GitHub</a>
</div>
    </div>
      </div>
  </div>
</template>

<script>
import ExperienceApp from "./components/Experience";
import ProjectApp from "./components/Project";
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
          src: "./img/html.png"
        },
        {
          id: 1,
          title: "Animacje w CSS nie są mi obce",
          src: "./img/css.png"
        },
        {
          id: 2,
          title: "API i Front pisze w JavaScript",
          src: "./img/JavaScript.png"
        },
        {
          id: 3,
          title: "Vue.js to framework który skradł mi serce",
          src: "./img/vue.png"
        },
        {
          id: 4,
          title: "Bootstrap bez niego życie nie było by takie proste",
          src: "./img/bootstrap.png"
        },
        {
          id: 5,
          title: "Dane pomiedzy api-front przesyłam jako JSON",
          src: "./img/json.png"
        },
        {
          id: 6,
          title: "GIT to System kontroli wersji który ratuje życie",
          src: "./img/Git.png"
        },
        {
          id: 7,
          title: "Do swoich projektów używam również TypeScript",
          src: "./img/typescript.png"
        },
        {
          id: 8,
          title: "API bez Node.js by nie istniało",
          src: "./img/node.png"
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
        alignToTop: "True",
        block: "start"
      });
    },
    hidenned() {
      if (this.ham != "menuspan col-sm-2 hidden") {
        this.ham = "menuspan col-sm-2 hidden";
      } else {
        this.ham = "menuspan hiddenbox col-sm-2";
      }
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
  cursor: pointer;
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
.hidden {
  display: block;
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
  padding-top: 13vh;
  height: 50vh;
  color: white;
  font-size: 2em;
}
.experience {
  text-align: center;
}
.experience h1 {
  padding-bottom: 50px;
  padding-top: 100px;
}
.chamburger {
  display: none;
}

.npm {
  width: 400px;
  display: inline-block;
  text-align: center;
  margin: 5px;
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
@media only screen and (max-width: 1000px) {
  .myphoto {
    width: 100%;
  }
  .myphoto img {
    transform: translateX(0%);
  }
  .about {
    width: 100%;
    font-size: 1.4em;
    padding-top: 0px;
  }
  h1 {
    padding-top: 100px;
  }
  .header {
    background-size: 150%;
    font-size: 2em;
  }
  .about {
    font-size: 1.3rem;
  }

  .menuspan {
    font-size: 1em;
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
}
</style>
