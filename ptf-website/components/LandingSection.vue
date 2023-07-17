<template>
  <section id="landing-section">
    <div class="landing-section__background">
      <img src="/background-circle.svg" class="landing-section__background-circle"/>
      <div class="landing-section__background-rectangle"></div>
    </div>
    <img src="/landing-page-logo.svg" class="landing-section__logo"/>

    <div class="landing-section__headers">
      <h1 class="landing-section__title">pens to friends</h1>
      <h1 class="landing-section__title landing-section__title--outline">pens to friends</h1>
    </div>

    <button class="landing-section__button" @click="getStarted">
      <span>Get Started</span>
      <img src="/arrow.svg" alt="">
    </button>

    <div class="landing-section__bottom-left">
      <div class="landing-section__line"></div>
      <div class="landing-section__smiles">
        <h2 class="landing-section__smiles-text">Spreading smiles, <br> one letter at a time</h2>
        <img src="/paper-aeroplane.svg" />
      </div>
    </div>
  </section>
</template>

<script setup>
function getStarted() {
  const router = useRouter()
  router.push({ path: "/GettingInvolved" });
}
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
  width: 34vw;
}

.landing-section__background-rectangle {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: #C8C8A9;
  opacity: 40%;
  z-index: -1;
  border: 1rem solid white;
}

.landing-section__logo {
  position: absolute;
  bottom: 0;
  right: 0;
  width: 34vw;
}

.landing-section__headers {
  position: absolute;
  left: 5vw;
  top: 5vh;
}

.landing-section__title {
  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 5rem;
  line-height: 3.125rem;
  display: flex;
  align-items: center;
  text-align: center;
  color: #A5A988;
  z-index: 2;
}

.landing-section__title--outline {
  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 5rem;
  line-height: 3.125rem;
  display: flex;
  align-items: center;
  text-align: center;
  color: transparent;
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: #A5A988;
}

.landing-section__button {
  top: 530px;
  left: 6.75rem;
  cursor: pointer;
  transition: all .2s;
  background: transparent;
  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 600;
  letter-spacing: 0.05rem;
  font-size: 1.5rem;
  line-height: 1.8125rem;
  display: flex;
  align-items: center;
  text-align: center;
  color: #35312B;
  border: 1px solid #A5A988;
  border-radius: 50%;
  padding: 1rem 2.5rem;
  height: 4rem;
  box-shadow: 5px 5px 0 0 #A5A988;
  z-index: 4;
}

#landing-section__button-link {
  text-align: center;
  color: #35312B;
  text-decoration: none;
  height: 4rem;
}

.landing-section__button>img {
  width: 2vw;
  margin-left: .5rem;
  transition: transform .3s ease-in-out;
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
  border: 5px solid #C8C8A9;
}

.landing-section__smiles {
  display: flex;
  flex-direction: row;
  z-index: 3;
}


.landing-section__smiles img {
  width: 10vw;
}
.landing-section__smiles-text {
  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 3rem;
  line-height: 4rem;
  margin-right: 1rem;
  color: #35312B;
}

@media only screen and (max-width: 480px) {

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
    width: 17rem;
    height: 0px;
    border: 2.5px solid #C8C8A9;
  }


  .landing-section__title,
  .landing-section__title--outline {
    font-size: 3.5rem;
    line-height: 4.2rem;
    margin: 0;
    width: fit-content;
    left: 2rem;
    width: 25rem;
    text-align: left;
  }

  .landing-section__button {
    top: 480px;
    left: 3rem;
    padding: 1rem 2.5rem;
    height: 3.5rem;
    width: fit-content;
    font-size: 1.25rem;
    box-shadow: 5px 5px 0 0 #A5A988;
    z-index: 4;
  }

  .landing-section__headers {
    left: 0;  
  }
}
</style>
