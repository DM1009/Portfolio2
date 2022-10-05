<template>


  <div id='navi'>
    <div class='navbar__logo'>
      <h2>DM</h2>
    </div>
    <ul class="navbar__menu">
      <li class="navbar__menu__item active" @click='moveScroll()' data-link="
        #home">
        Home
      </li>
      <li class="navbar__menu__item" @click='moveScroll()' data-link="
        #about">
        About
      </li>
      <li class="navbar__menu__item" @click='moveScroll()' data-link="
        #skills">
        Skills
      </li>
      <li class="navbar__menu__item" @click='moveScroll()' data-link="
        #work">
        Work
      </li>
    </ul>
  </div>
  <home id='home' />
  <about id='about' />
  <skill id='skills' />
  <project id='work' />

  <div class="ocean">

    <div class="wave"></div>
    <div class="wave"></div>
  </div>
</template>

<script>
import home from './components/PFHome.vue'
import about from './components/PFAbout.vue'
import skill from './components/PFSkill.vue'
import project from './components/PFProject.vue'



export default {
  name: 'App',
  components: {
    home,
    about,
    skill,
    project,

  },
  methods: {
    scrollIntoView(selector) {
      const scrollTo = document.querySelector(selector);
      scrollTo.scrollIntoView({ behavior: 'smooth' });
    },
    navbarHeight() {
      const navbar = document.querySelector('#navi')
      if (window.scrollY > 100) {
        navbar.classList.add('navbar_dark');
      } else {
        navbar.classList.remove('navbar_dark');
      }
    },

    moveScroll() {
      const navbarMenu = document.querySelector('.navbar__menu');
      navbarMenu.addEventListener('click', (event) => {
        const target = event.target;
        const link = target.dataset.link;
        if (link == null) {
          return;
        }
        navbarMenu.classList.remove('open');
        this.scrollIntoView(link);
      });


    },

  },
  mounted() {
    document.addEventListener('scroll', this.navbarHeight)

  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Jua');

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}

body {
  background: radial-gradient(ellipse at center, rgb(255, 255, 255) 0%, rgb(255, 255, 255) 35%, #d2ecf7 100%);
}

h2 {
  font-family: 'SDSamliphopangche_Outline';
}

h5 {
  font-family: 'SDSamliphopangche_Outline';
}

.ocean {
  height: 1%;
  width: 100%;
  position: fixed;
  bottom: -100px;
  left: 0;
  background: #015871;
  opacity: 20%;
}

.wave {
  background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/85486/wave.svg) repeat-x;
  position: absolute;
  top: -198px;
  width: 6400px;
  height: 198px;
  animation: wave 7s cubic-bezier(0.36, 0.45, 0.63, 0.53) infinite;
  transform: translate3d(0, 0, 0);
}

.wave:nth-of-type(2) {
  top: -175px;
  animation: wave 7s cubic-bezier(0.36, 0.45, 0.63, 0.53) -.125s infinite, swell 7s ease -1.25s infinite;
  opacity: 1;
}

@keyframes wave {
  0% {
    margin-left: 0;
  }

  100% {
    margin-left: -1600px;
  }
}

@keyframes swell {

  0%,
  100% {
    transform: translate3d(0, -25px, 0);
  }

  50% {
    transform: translate3d(0, 5px, 0);
  }
}

ul {
  list-style: none;
  margin-top: 10px;
  z-index: 2;
}


#navi li {
  font-size: 20px;
}

#navi {
  position: fixed;
  width: 100%;
  background-color: transparent;
  align-items: center;
  padding: 16px;
  z-index: 1;
  color: rgb(2, 149, 247);
  transition: 300ms ease-in;
  height: 6%;
  display: flex;
  justify-content: space-between;

}



.navbar__logo {
  margin-top: 10px;
}

#navi.navbar_dark {
  background-color: rgb(2, 149, 247);
  color: white;

}

.navbar__menu {
  display: flex;

}

.navbar__menu__item {
  padding: 8px 12px;
  margin: 4px 4px;
  cursor: pointer;
  border-radius: 4px;

}

.navbar__menu__item:hover {
  background-color: rgb(2, 149, 247);
  border-radius: 4px;
  color: white;
}

@font-face {
  font-family: 'SDSamliphopangche_Outline';
  src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts-20-12@1.0/SDSamliphopangche_Outline.woff') format('woff');
  font-weight: normal;
  font-style: normal;
}

@media screen and (max-width: 768px) {
  #navi li {
    font-size: 15px;
  }

  .navbar__menu__item {
    padding: 8px 3px;
    margin: 3px 3px;
    cursor: pointer;
    border-radius: 4px;

  }
}
</style>
