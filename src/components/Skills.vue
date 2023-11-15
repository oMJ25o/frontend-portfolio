<template>
  <!-- Skills Section -->
  <section class="section-skills" id="section-skills" style="scroll-margin-top: 11vh">
    <div class="container-skill" id="container-skill">
      <div class="container-content-header" id="container-content-header">
        <p class="explore-my-text" id="explore-my-text">Explore My</p>
        <p class="skill-text">Skills</p>
      </div>
    </div>
    <div class="container-content-main" id="container-content-main">
      <div class="container-frontend-skills" id="container-frontend-skills">
        <p class="frontend-text" id="frontend-text">Frontend Development Skills</p>
        <div class="container-frontend-content" id="container-frontend-content">
          <div
            v-for="skill in frontendSkills"
            :skill="skill"
            class="container-skill"
            id="container-skill"
          >
            <span
              class="proficiency-bar"
              id="proficiency-bar"
              :style="{ backgroundImage: skill.proficiencyStyle }"
            ></span>
            <div class="container-skill-content" id="container-skill-content">
              <p class="frontend-skill-name" id="frontend-skill-name">{{ skill.name }}</p>
            </div>
          </div>
        </div>
      </div>
      <div class="container-other-skills" id="container-other-skills">
        <p class="other-text" id="other-text">Other Skills</p>
        <div class="container-other-content" id="container-other-content">
          <div
            v-for="skill in otherSkills"
            :skill="skill"
            class="container-skill"
            id="container-skill"
          >
            <span
              class="proficiency-bar"
              id="proficiency-bar"
              :style="{ backgroundImage: skill.proficiencyStyle }"
            ></span>
            <div class="container-skill-content" id="container-skill-content">
              <p class="other-skill-name" id="other-skill-name">{{ skill.name }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container-arrow" id="container-arrow">
      <a href="#section-contact"><img id="arrow-pic" src="../assets/arrow.png" /></a>
    </div>
  </section>
</template>

<script>
import { ref, reactive } from 'vue'
// Make a list for both frontend skills and other skills
// Frontend-Skills - HTML, CSS, JS, Vue
// Other Skills - GitHub, C#,  Teamwork, Communication, Time-management
export default {
  data() {
    return {
      frontendSkills: [
        {
          name: 'HTML',
          proficiencyStyle: `linear-gradient(to right, red 70%, white 30%)`
        },
        {
          name: 'CSS',
          proficiencyStyle: `linear-gradient(to right, red 55%, white 45%)`
        },
        {
          name: 'Javascript',
          proficiencyStyle: `linear-gradient(to left, white 60%, red 40%)`
        },
        {
          name: 'Vue',
          proficiencyStyle: `linear-gradient(to left, white 60%, red 40%)`
        }
      ],
      otherSkills: [
        {
          name: 'GitHub',
          proficiencyStyle: `linear-gradient(to right, red 60%, white 35%)`
        },
        {
          name: 'C#',
          proficiencyStyle: `linear-gradient(to right, red 75%, white 25%)`
        },
        {
          name: 'Teamwork',
          proficiencyStyle: `linear-gradient(to right, red 50%, white 50%)`
        },
        {
          name: 'Communication',
          proficiencyStyle: `linear-gradient(to right, red 55%, white 45%)`
        },
        {
          name: 'Time-Management',
          proficiencyStyle: `linear-gradient(to right, red 55%, white 45%)`
        }
      ]
    }
  }
}
</script>

<style scoped>
.section-skills,
.container-skill-content,
.container-content-header,
.container-frontend-skills,
.container-other-skills {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.section-skills {
  height: 100vh;
}

.container-content-header {
  margin-top: 2rem;
}

.container-content-header p:first-child {
  font-size: calc(0.6rem + 1.5vmin);
}
.container-content-header p:last-child {
  font-size: calc(0.6rem + 5vmin);
  font-weight: bold;
}

.container-content-main {
  display: flex;
  justify-content: space-around;
  gap: 1rem;
}

.container-frontend-skills,
.container-other-skills {
  width: 40vw;
  height: 60vh;
  border: 1px solid gray;
  border-radius: 20px;
  margin-top: 1.5rem;
}

.container-frontend-content,
.container-other-content {
  width: 40vw;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  margin-top: 3rem;
  gap: 2rem;
}

.container-other-content {
  gap: 1.5rem;
}

.container-skill {
  display: flex;
  justify-content: space-around;
  align-items: center;
  gap: 0.5rem;
}

.proficiency-bar {
  width: 15vw;
  height: 3vh;
  border: 2px solid black;
  border-radius: 20px;
}

.container-skill-content {
  width: 11vw;
  align-items: start;
}

.container-arrow {
  margin-top: 5vh;
}

.explore-my-text {
  color: rgb(126, 102, 102);
}

.skill-text {
  color: black;
}

.achievement-icon {
  width: fit-content;
  height: 2vw;
  margin-top: 0.5rem;
}

.frontend-skill-name,
.other-skill-name {
  font-size: calc(0.75rem + 1vmin);
  font-weight: bold;
  color: rgb(126, 102, 102);
}

.frontend-skill-proficiency,
.other-skill-proficiency {
  font-size: calc(0.5rem + 1vmin);
}

.frontend-text,
.other-text {
  font-size: calc(0.75rem + 2vmin);
  font-weight: bold;
  margin-top: 1rem;
  color: rgb(126, 102, 102);
}
</style>
