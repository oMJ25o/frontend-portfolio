<template>
  <!-- Contact Section -->
  <section class="section-contact" id="section-contact" style="scroll-margin-top: 5vh">
    <div class="container-contact-text" id="container-contact-text">
      <p class="get-in-touch-text" id="get-in-touch-text">Get in Touch</p>
      <p class="contact-me-text" id="contact-me-text">Contact Me</p>
      <div class="container-contact-links" id="container-contact-links">
        <div
          v-for="contact in contactLinks"
          :contact="contact"
          class="container-link-items"
          id="container-link-items"
        >
          <img class="contact-icon" id="contact-icon" src="../assets/email.png" />
          <p class="contact-name" id="contact-name">
            <a :href="contact.url" :target="contact.target">{{ contact.name }}</a>
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { ref } from 'vue'

export default {
  data() {
    return {
      contactLinks: [
        {
          name: 'menardaustero@gmail.com',
          target: ''
        }
      ]
    }
  }
}
</script>

<style scoped>
p,
a {
  color: black;
}

a {
  text-decoration-line: none;
}

a:hover {
  text-decoration: underline;
  text-underline-offset: 1vh;
}

.section-contact {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container-contact-text {
  text-align: center;
}

.container-contact-links {
  display: flex;
  align-items: center;
}

.container-contact-links {
  margin-top: 3rem;
  width: 25vw;
  height: 10vh;
  border: 1px solid rgb(126, 102, 102);
  border-radius: 25px;
  justify-content: space-around;
}

.container-link-items {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.get-in-touch-text {
  font-size: calc(0.75rem + 1vmin);
  color: rgb(126, 102, 102);
}

.contact-me-text {
  font-size: calc(0.75rem + 3.5vmin);
  font-weight: bold;
}

.contact-icon {
  width: 2vw;
  height: 4vh;
}

.contact-name {
  font-size: calc(0.75rem + 1vmin);
  font-weight: bold;
}
</style>
