<template>
  <div class="container__menu">
    <div class="container__menu-icon">
      <label class="burger" for="burger">
        <input type="checkbox" id="burger" />
        <span></span>
        <span></span>
        <span></span>
      </label>
    </div>
    <div class="container__navMenu-links">
      <div class="container__navMenu-link home-link">
        <img src="/home.png" alt="Home" />
        <nuxt-link @click="closeMenu" to="/" draggable="false">Home</nuxt-link>
      </div>
      <div class="container__navMenu-link involved-link">
        <img src="/messenger.png" alt="Home" />
        <nuxt-link @click="closeMenu" to="/GettingInvolved" draggable="false"
          >Get Involved</nuxt-link
        >
      </div>
      <div class="container__navMenu-link faq-link">
        <img src="/question.png" alt="Home" />
        <nuxt-link @click="closeMenu" to="/FrequentQuestions" draggable="false"
          >FAQs</nuxt-link
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    closeMenu() {
      const checkbox = document.getElementById("burger");
      const navMenu = document.querySelector(".container__navMenu-links");

      checkbox.checked = false;
      navMenu.classList.remove("container__navMenu-links-active");
      document.body.classList.remove("body-no-scroll");
    },
  },
  mounted() {
    const checkbox = document.getElementById("burger");
    const navMenu = document.querySelector(".container__navMenu-links");

    checkbox.addEventListener("click", () => {
      if (checkbox.checked) {
        document.body.classList.add("body-no-scroll");
        navMenu.classList.add("container__navMenu-links-active");
        setTimeout(() => {
          navMenu.classList.add("container__navMenu-links-active-fadeIn");
          navMenu.classList.remove("container__navMenu-links-active-fadeOut");
        }, 10);
      } else {
        document.body.classList.remove("body-no-scroll");
        navMenu.classList.add("container__navMenu-links-active-fadeOut");
        navMenu.classList.remove("container__navMenu-links-active-fadeIn");
        setTimeout(() => {
          navMenu.classList.remove("container__navMenu-links-active");
        }, 250);
      }
    });
  },
};
</script>

<style>
.body-no-scroll {
  overflow: hidden;
}

.container__menu {
  font-family: "Montserrat", sans-serif;
  width: 100vw;
  opacity: 1;
}

.container__menu-icon {
  padding-left: 0.8rem;
  padding-top: 0.8rem;
  z-index: 5;
}

.container__navMenu-links {
  display: none;
  width: 100vw;
  height: 100vh;
  padding-top: 10vh;
  padding-left: 2rem;

  flex-direction: column;

  background-color: #c8c8a9;
}

.container__navMenu-links a {
  padding: 1rem 1rem;
  font-size: 1.6rem;
  color: black;
  text-decoration: none;
}

.container__navMenu-link {
  display: flex;
  align-items: center;
}

.container__navMenu-link img {
  height: 30px;
}

.container__navMenu-links-active {
  opacity: 0;
  display: flex;
  position: fixed;
  top: 0;
  z-index: 3;
}

.container__navMenu-links-active-fadeIn {
  transition: opacity 0.25s ease-in-out;
  opacity: 1;
}

.container__navMenu-links-active-fadeOut {
  transition: opacity 0.25s ease-in-out;
  opacity: 0;
}

/* menu icon stuff */
.burger {
  position: relative;
  width: 40px;
  height: 30px;
  background: transparent;
  cursor: pointer;
  display: block;
}

.burger input {
  display: none;
}

.burger span {
  display: block;
  position: absolute;
  height: 4px;
  width: 100%;
  background: #a5a988;
  border-radius: 9px;
  opacity: 1;
  left: 0;
  transform: rotate(0deg);
  transition: 0.25s ease-in-out;
}

.burger span:nth-of-type(1) {
  top: 0px;
  transform-origin: left center;
}

.burger span:nth-of-type(2) {
  top: 50%;
  transform: translateY(-50%);
  transform-origin: left center;
}

.burger span:nth-of-type(3) {
  top: 100%;
  transform-origin: left center;
  transform: translateY(-100%);
}

.burger input:checked ~ span:nth-of-type(1) {
  transform: rotate(45deg);
  top: 0px;
  left: 5px;
}

.burger input:checked ~ span:nth-of-type(2) {
  width: 0%;
  opacity: 0;
}

.burger input:checked ~ span:nth-of-type(3) {
  transform: rotate(-45deg);
  top: 28px;
  left: 5px;
}

@media only screen and (min-width: 1200px) {
  .container__menu {
    display: none;
  }
}

@media only screen and (min-width: 721px) and (max-width: 1200px) {
  .container__menu {
    display: flex;
  }
  .container__menu-icon {
    transform: scale(2);
    padding-left: 1.5rem;
    padding-top: 1.5rem;
  }
  .container__navMenu-links a {
    font-size: 3rem;
  }

  .container__navMenu-link img {
    height: 50px;
  }
}
</style>
