<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
function toggleMenu() {
  const menu = document.querySelector(".menu-links");
  const icon = document.querySelector(".hamburger-icon");
  menu.classList.toggle("open");
  icon.classList.toggle("open");
}
</script>

<template>
 <nav id="desktop-nav">
      <div class="logo">Saad Qayyum</div>
      <div>
        <ul class="nav-links">
          <li><a href="#about">About</a></li>
          <li><a href="#experience">Experience</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div>
    </nav>
    <nav id="hamburger-nav">
      <div class="logo">John Doe</div>
      <div class="hamburger-menu">
        <div class="hamburger-icon" onclick="toggleMenu()">
          <span></span>
          <span></span>
          <span></span>
        </div>
        <div class="menu-links">
          <li><a href="#about" onclick="toggleMenu()">About</a></li>
          <li><a href="#experience" onclick="toggleMenu()">Experience</a></li>
          <li><a href="#projects" onclick="toggleMenu()">Projects</a></li>
          <li><a href="#contact" onclick="toggleMenu()">Contact</a></li>
        </div>
      </div>
    </nav>
    <section id="profile">
      <div class="section__pic-container">
        <img src="../assets/DP.png" alt="Saad Qayyum profile picture" />
      </div>
      <div class="section__text">
        <p class="section__text__p1">Hello, I'm</p>
        <h1 class="title">Saad Qayyum</h1>
        <p class="section__text__p2">Full Stack Developer</p>
        <div class="btn-container">
          <button 
            class="btn btn-color-2"
            onclick="window.open('khawajasaadqayyum4110@gmail.com')"

          >
            Download CV
          </button>
          <button class="btn btn-color-1" onclick="location.href='./#contact'">
            Contact Info
          </button>
        </div>
        <div id="socials-container">
          <img
            src="../assets/linkedin.png"
            alt="My LinkedIn profile"
            class="icon"
            onclick="location.href='https:/linkedin.com/in/saad-qayyum4110'"
          />
          <img
            src="../assets/github.png"
            alt="My Github profile"
            class="icon"
            onclick="location.href='https:/github.com/KhawajaSaadQayyum'"
          />
        </div>
      </div>
    </section>
    
   
  

    


 
</template>

<style scoped>
.read-the-docs {
  color: #888;
}

</style>
