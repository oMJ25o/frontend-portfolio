<template>
  <!-- Navigation Menu -->
  <nav class="navbar-menu" id="navbar-menu">
    <div class="logo">Menard Austero</div>
    <ul class="nav-links">
      <li v-for="link in navMenu" :link="link">
        <a :href="link.url" onclick="toggleMenu">{{ link.name }}</a>
      </li>
    </ul>
  </nav>
  <nav id="hamburger-nav">
    <div class="logo">Menard Austero</div>
    <div class="hamburger-menu">
      <div class="hamburger-icon" id="hamburger-icon" :onclick="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
      </div>
      <!-- Hamburger Menu -->
      <div>
        <ul class="menu-links">
          <li v-for="link in navMenu" :link="link">
            <a :href="link.url" onclick="toggleMenu">{{ link.name }}</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      navMenu: [
        {
          name: 'About',
          url: '#section-about'
        },
        {
          name: 'Skills',
          url: '#section-skills'
        },
        {
          name: 'Contact',
          url: '#section-contact'
        }
      ]
    }
  },
  methods: {
    toggleMenu() {
      const menu = document.querySelector('.menu-links')
      const icon = document.querySelector('.hamburger-icon')
      menu.classList.toggle('open')
      icon.classList.toggle('open')
    }
  }
}
</script>

<style scoped>
.logo,
p,
li,
a {
  color: black;
}

a {
  text-decoration-line: none;
}

a:hover {
  color: gray;
  text-decoration-line: underline;
  text-underline-offset: 1rem;
}

nav,
.nav-links {
  display: flex;
}

nav {
  justify-content: space-around;
  align-items: center;
  height: 10vh;
  background-color: white;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.2);
  position: fixed;
  top: 0px;
}

.navbar-menu {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo {
  font-size: calc(0.75rem + 2vmin);
  font-weight: bold;
  margin: 3.5vh 0rem 0rem 15vw;
  flex-grow: 1;
  cursor: default;
}

.nav-links {
  margin: 2rem 15rem 0rem 0rem;
  gap: 2rem;
  list-style: none;
  font-size: calc(0.75rem + 2vmin);
}

/* #hamburger-nav {
  display: none;
} */

.hamburger-menu {
  position: relative;
  display: flex;
  align-items: center;
}

.hamburger-icon {
  margin: 2.5rem 3rem 0rem 0rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 24px;
  width: 30px;
  cursor: pointer;
}

.hamburger-icon span {
  width: 100%;
  height: 0.3vh;
  background-color: black;
  transition: all 0.3 ease-in-out;
}

.menu-links {
  position: absolute;
  top: 100%;
  right: 100%;
  background-color: white;
  width: fit-content;
  max-height: 0;
  overflow: hidden;
  transition: all 0.3 ease-in-out;
}

.menu-links a {
  display: block;
  padding: 10px;
  text-align: center;
  font-size: calc(0.75rem + 1.5vmin);
  color: black;
  transition: all 0.3 ease-in-out;
}

.menu-links li {
  list-style: none;
}

.menu-links.open {
  max-height: 400px;
}

.hamburger-icon.open span:first-child {
  transform: rotate(45deg) translate(10px, 5px);
}
.hamburger-icon.open span:nth-child(2) {
  opacity: 0;
}
.hamburger-icon.open span:last-child {
  transform: rotate(-45deg) translate(10px, -5px);
}

.hamburger-icon span:first-child {
  transform: none;
}
.hamburger-icon span:first-child {
  opacity: 1;
}
.hamburger-icon span:first-child {
  transform: none;
}
</style>
