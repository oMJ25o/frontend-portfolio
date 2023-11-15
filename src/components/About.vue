<template>
  <!-- About Section -->
  <section class="section-about" id="section-about" style="scroll-margin-top: 5vh">
    <div class="container-about-header" id="container-about-header">
      <p>Get To Know More</p>
      <p>About Me</p>
    </div>
    <div class="container-about-main" id="container-about-main">
      <div class="about-pic" id="about-pic">
        <img class="about-picture" id="about-picture" src="../assets/aboutpicture.jpg" />
      </div>
      <div class="container-about-content" id="container-about-content">
        <div class="container-achievements" id="container-achievements">
          <div class="container-education" id="container-education">
            <img class="education-icon" id="education-icon" src="../assets/educationicon.png" />
            <p>Education</p>
            <p>Bachelor's Degree in Computer Science</p>
            <p>2018 - 2023</p>
          </div>
        </div>
        <p class="about-me-text" id="about-me-text">
          Hello There! I'm Menard Jesse Austero, a junior frontend developer with a passion for
          creating engaging and user-friendly digital experiences. I thrive on turning ideas into
          interactive and visually appealing websites. I love exploring new technologies and
          learning the latest trends in frontend development. I enjoy the dynamic nature of the
          field. I'm currently on a continuous learning journey and currently diving deeper into the
          frontend development.
        </p>
      </div>
    </div>
    <div class="container-arrow" id="container-arrow">
      <a href="#section-skills"
        ><img class="arrow-pic" id="arrow-pic" src="../assets/arrow.png"
      /></a>
    </div>
  </section>
</template>

<script></script>

<style scoped>
.section-about,
.container-about-header,
.container-about-main,
.container-education,
.container-achievements {
  display: flex;
}

.section-about,
.container-about-header {
  flex-direction: column;
  align-items: center;
}

.section-about {
  height: 100vh;
}

.container-about-header {
  margin-top: 3rem;
}

.container-about-header p:first-child {
  font-size: calc(0.65rem + 1.75vmin);
  color: rgb(126, 102, 102);
}
.container-about-header p:last-child {
  font-size: calc(0.65rem + 5vmin);
  font-weight: bold;
  color: black;
}

.container-about-main {
  justify-content: center;
  align-items: center;
  margin: 5rem 10rem 1rem 10rem;
  gap: 2rem;
}

.container-achievements {
  justify-content: center;
  margin-bottom: 2rem;
}

.container-education {
  width: 30vw;
  height: 17vh;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border: 1.5px solid black;
  border-radius: 20px;
  text-align: center;
}

.container-education p,
.container-about-main p {
  color: black;
}

.about-picture {
  width: fit-content;
  height: 55vh;
  border-radius: 25px;
  margin-right: 3rem;
}

.education-icon {
  width: 3vw;
  height: 6vh;
}

.about-me-text {
  width: 45vw;
  text-align: justify;
  font-size: calc(0.45rem + 1vmin);
}
</style>
