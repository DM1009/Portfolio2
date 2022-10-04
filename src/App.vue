<template>
  <div id='navi'>
    <div class='navbar__logo'>
      <h2>DM</h2>
    </div>
    <ul class="navbar__menu">
      <li class="navbar__menu__item active" @click='moveScroll(0)' data-link="
        #home">
        Home
      </li>
      <li class="navbar__menu__item" @click='moveScroll(832)' data-link="
        #about">
        About
      </li>
      <li class="navbar__menu__item" @click='moveScroll(1652)' data-link="
        #skills">
        Skills
      </li>
      <li class="navbar__menu__item" @click='moveScroll(2527)' data-link="
        #work">
        Work
      </li>
      <li class="navbar__menu__item">
        Contact
      </li>
    </ul>
  </div>
  <home id='home' />
  <about id='about' />
  <skill id='skills' />
  <project id='work' />

</template>

<script>
import home from './components/PFHome.vue'
import about from './components/PFAbout.vue'
import skill from './components/PFSkill.vue'
import project from './components/PFProject.vue'

export default {
  name: 'App',
  components: {
    home, about, skill, project
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


    }
  },
  mounted() {
    document.addEventListener('scroll', this.navbarHeight)

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}

ul {
  list-style: none;
  margin-top: 10px;

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
