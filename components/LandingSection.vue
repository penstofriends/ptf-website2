<template>
  <section id="landing-section">
    <div class="landing-section__background">
      <img
        src="/background-circle.svg"
        class="landing-section__background-circle"
        width="650"
      />
      <div class="landing-section__background-rectangle"></div>
    </div>
    <img
      src="/landing-page-logo.svg"
      class="landing-section__logo"
      width="650"
    />

    <div class="landing-section__headers">
      <h1 class="landing-section__title">pens to friends</h1>
      <h1 class="landing-section__title landing-section__title--outline">
        pens to friends
      </h1>
    </div>

    <button class="landing-section__button" @click="getStarted">
      <span>Get Started</span>
      <img src="/arrow.svg" alt="" />
    </button>

    <div class="landing-section__bottom-left">
      <div class="landing-section__line"></div>
      <div class="landing-section__smiles">
        <h2 class="landing-section__smiles-text">
          Spreading smiles, one letter at a time
        </h2>
        <img width="146" src="/paper-aeroplane.svg" />
      </div>
    </div>
  </section>
</template>

<script setup>
function getStarted() {
  const router = useRouter();
  router.push({ path: "/GettingInvolved" });
}
onMounted(() => {
  const bottomLeft = document.querySelector(".landing-section__bottom-left");
  if (screen.width < 1200 && screen.width > 720) {
    bottomLeft.classList.add("onLeft");
    setTimeout(() => {
      bottomLeft.classList.add("slideRight");
    }, 1000);
  }
});
</script>

<style scoped>
#landing-section {
  width: 100vw;
  height: 100vh;
  display: flex;
  position: relative;
}

.landing-section__background {
  position: relative;
}

.landing-section__background-circle {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
}

.landing-section__background-rectangle {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: #c8c8a9;
  opacity: 40%;
  z-index: -1;
  border: 1rem solid white;
}

.landing-section__logo {
  position: absolute;
  bottom: 0;
  right: 0;
}

.landing-section__headers {
  position: absolute;
  left: 260px;
  top: 100px;
}

.landing-section__title {
  font-family: "Montserrat", sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 8rem;
  line-height: 3.125rem;
  display: flex;
  align-items: center;
  text-align: center;
  color: #a5a988;
  z-index: 2;
}

.landing-section__title--outline {
  font-family: "Montserrat", sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 8rem;
  line-height: 3.125rem;
  display: flex;
  align-items: center;
  text-align: center;
  color: transparent;
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: #a5a988;
}

.landing-section__button {
  top: 530px;
  left: 6.75rem;
  cursor: pointer;
  transition: all 0.2s;
  background: transparent;
  font-family: "Montserrat", sans-serif;
  font-style: normal;
  font-weight: 600;
  letter-spacing: 0.05rem;
  font-size: 1.5rem;
  line-height: 1.8125rem;
  display: flex;
  align-items: center;
  text-align: center;
  color: #35312b;
  border: 1px solid #a5a988;
  border-radius: 50%;
  padding: 1rem 2.5rem;
  height: 4rem;
  box-shadow: 5px 5px 0 0 #a5a988;
  z-index: 4;
}

#landing-section__button-link {
  text-align: center;
  color: #35312b;
  text-decoration: none;
  height: 4rem;
}

.landing-section__button > img {
  width: 2.125rem;
  margin-left: 0.5rem;
  transition: transform 0.3s ease-in-out;
}

.landing-section__button:hover img {
  transform: translateX(5px);
}

.landing-section__button:active {
  transform: scale(0.95);
}

.landing-section__bottom-left {
  position: absolute;
  padding: 2.5rem 5rem;
  bottom: 0;
  left: 0;
  display: flex;
  flex-direction: column;
}

.landing-section__line {
  position: absolute;
  width: 27.125rem;
  height: 0px;
  border: 5px solid #c8c8a9;
}

.landing-section__smiles {
  display: flex;
  flex-direction: row;
  z-index: 3;
}

.landing-section__smiles-text {
  font-family: "Montserrat", sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 4rem;
  line-height: 7.1875rem;
  color: #35312b;
  width: 38.1875rem;
  height: 12.5rem;
}

/* mobile */

@media only screen and (max-width: 720px) {
  .landing-section__background-circle {
    width: 85vw;
  }

  .landing-section__logo {
    display: none;
  }

  .landing-section__bottom-left {
    width: 4rem;
    padding: 2.5rem;
  }

  .landing-section__bottom-left img {
    width: 6rem;
  }

  .landing-section__smiles-text {
    font-size: 2rem;
    line-height: 3rem;
  }

  .landing-section__line {
    width: 80vw;
    height: 0px;
    border: 2.5px solid #c8c8a9;
  }

  .landing-section__title,
  .landing-section__title--outline {
    font-size: 3.5rem;
    line-height: 4.2rem;
    width: 80vw;
    margin: 0;
    left: 2rem;
    text-align: left;
  }

  .landing-section__button {
    top: 50vh;
    left: 3rem;
    padding: 1rem 2.5rem;
    height: 3.5rem;
    width: fit-content;
    font-size: 1.25rem;
    box-shadow: 5px 5px 0 0 #a5a988;
    z-index: 4;
  }

  .landing-section__headers {
    left: 0;
    top: 10vh;
  }
}

/* more mobile but for shorter ones */

@media only screen and (max-height: 730px) {
  .landing-section__title {
    font-size: 3rem;
    line-height: initial;
  }

  .landing-section__smiles-text {
    font-size: 2rem;
    line-height: initial;

    height: 20vh;
  }
  .landing-section__smiles img {
    height: 30vh;
  }
}

@media only screen and (min-width: 721px) and (max-width: 1200px) {
  #landing-section {
    height: 100vh;
  }
  .landing-section__headers {
    left: 50px;
    top: 60px;
    
    margin-left: 5vw;
  }
  .landing-section__background-circle {
    height: 40vh;
  }
  .landing-section__smiles-text {
    font-size: 2rem;
    line-height: 4rem;
    width: 40vw;
  }
  .landing-section__line {
    width: 50vw;
  }
  .landing-section__button {
    top: 65vh;
  }
  .landing-section__title {
    font-size: 7rem;
    margin: 0;
    text-align: initial;
    line-height: normal;
  }
  .landing-section__logo {
    height: 50vh;
    opacity: .5;
  }

  .onLeft {
    transform: translateX(-100%);
  }

  .slideRight {
    transform: translateX(0%);
    animation: slideRight 1s;
  }

  .onRight {
    transform: translateX(0%);
  }

  @keyframes slideRight {
    0% {
      transform: translateX(-100%);
    }

    100% {
      transform: translateX(0%);
    }
  }
}
</style>
