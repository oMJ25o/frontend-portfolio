<template>
  <!-- Intro Section -->
  <section class="container-profile" id="container-section">
    <div class="container-profile-main" id="container-profile-main">
      <div class="container-pic" id="container-pic">
        <img
          class="profile-pic"
          id="profile-pic"
          src="../assets/profilepicture.png"
          alt="My Profile Picture"
        />
      </div>
      <div class="container-profile-text">
        <p class="hello-text" id="hello-text">Hello, I am</p>
        <p class="name-text" id="name-text">Menard Austero</p>
        <p class="main-role" id="main-role">Junior Frontend Developer</p>
        <div class="container-btns">
          <a class="btn-contact" id="btn-contact" href="#section-contact">Contact Info</a>
        </div>
      </div>
    </div>
    <div class="container-arrow">
      <a href="#section-about"><img id="arrow-pic" src="../assets/arrow.png" /></a>
    </div>
  </section>
</template>

<script>
import { ref } from 'vue'

export default {
  data() {
    const cvFile = ref('../cv.pdf')
    return {
      cvFile,
      socialLinks: [
        {
          name: 'LinkedIn',
          url: 'https://www.linkedin.com/in/menard-austero',
          src: ref('../linkedin-black.png')
        },
        {
          name: 'ItchIO',
          url: 'https://omjo.itch.io',
          src: ref('../itchio-black.png')
        }
      ]
    }
  }
}
</script>

<style>
.container-profile,
.container-profile-main,
.container-profile-text,
.container-arrow {
  display: flex;
}

.container-profile {
  width: 100dvw;
  height: 100vh;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.container-pic {
  margin-bottom: 15vh;
}

.container-profile-main {
  justify-content: center;
  align-items: center;
  height: 75vh;
  margin-top: 5rem;
}

.container-profile-text {
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.container-profile-text p:first-child {
  color: rgb(126, 102, 102);
  font-size: calc(0.75rem + 2vmin);
}
.container-profile-text p:nth-child(2) {
  font-size: calc(0.75rem + 3vmin);
  font-weight: bold;
  color: black;
}
.container-profile-text p:nth-child(3) {
  font-size: calc(0.75rem + 2vmin);
  color: rgb(126, 102, 102);
  font-weight: bold;
}

.profile-pic {
  background-color: rgb(126, 102, 102);
  border-radius: 50%;
  max-height: fit-content;
  height: 50vh;
  width: 25vw;
  margin-top: 15vh;
  margin-right: 5vw;
}

.container-btns {
  display: flex;
  justify-content: space-around;
  gap: 2rem;
  margin-top: 3vh;
}

.btn-contact {
  width: 15vw;
  text-align: center;
  padding: 1rem;
  color: white;
  border: 1px solid black;
  background-color: rgb(126, 102, 102);
  font-size: calc(0.75rem + 1.2vmin);
  font-weight: 600;
  transition: all 0.2s ease;
  border-radius: 30px;
  text-decoration: none;
}

#btn-contact:hover {
  background-color: rgb(65, 52, 52);
  text-decoration-line: none;
}

.container-social-links {
  width: 10vw;
}

.social-list {
  margin-top: 2rem;
  padding-left: 0;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.social-links-list {
  list-style: none;
}

.social-pic {
  width: 2vw;
  height: 4vh;
}
</style>
