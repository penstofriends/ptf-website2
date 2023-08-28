<template>
  <div class="navbar-container">
    <nav class="container__navTab-links">
      <div class="links">
        <nuxt-link to="/" draggable="false">Home</nuxt-link>
        <nuxt-link to="/GettingInvolved" draggable="false">Get Involved</nuxt-link>
        <nuxt-link to="/FrequentQuestions" draggable="false">FAQs</nuxt-link>
      </div>
      <div class="contacts">
        <a href="https://mail.google.com/mail/u/1/?view=cm&fs=1&to=penstofriends@gmail.com&tf=1"
          target="_blank" rel="noopener">
          <img src="/email.svg" alt="email/envelope icon" width="35" class="social-icon">
        </a>
        <a href="https://www.instagram.com/penstofriends/" target="_blank" rel="noopener">
          <img src="/instagram.svg" alt="instagram icon" width="30" class="social-icon">
        </a>
        <a href="https://www.tiktok.com/@penstofriends" target="_blank" rel="noopener">
          <img src="/tiktok.svg" alt="tiktok icon" width="25" class="social-icon">
        </a>
      </div>
    </nav>
  </div>
</template>

<style scoped>
.navbar-container {
  padding: 0 1.5rem;
  background-color: white;
}

.container__navTab-links {
  font-family: 'Open Sans', sans-serif;
  font-weight: 500;
  letter-spacing: 0.1rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-align: center;
  padding: 1rem 0rem;
  z-index: 3;
}

.links {
  display: flex;
  align-items: center;
}

.container__navTab-links a {
  font-size: 1.2rem;
  color: #C8C8A9;
  padding: 0 1rem;
  margin: 0 0.5rem;
  text-decoration: none;
  transition: color 0.3s ease-in-out;
}

.container__navTab-links a:first-of-type {
  border: none;
}

.container__navTab-links a.router-link-exact-active {
  color: var(--turfGreen);
}

.container__navTab-links a.router-link-exact-active:hover {
  background-color: transparent;
}

.container__navTab-links a:hover {
  transition: 1s;
  opacity: 0.6;
}

.contacts {
  display: flex;
  align-items: center;
}

.contacts a {
  display: flex;
  align-items: center;
}

.contacts img {
  margin: 0 0.2rem; 
  transition: transform 0.3s ease-in-out;
}

.contacts img:hover {
  transform: scale(1.05);
}

@media only screen and (max-width: 1200px) {
  .container__navTab-links {
    display: none;
  }
}
</style>
