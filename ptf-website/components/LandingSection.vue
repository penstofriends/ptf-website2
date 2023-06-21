<template>
  <section id="section__landingSection">
    <div class="container__landingSection">
      <div class="headers">
        <h1>pens to friends</h1>
        <h1 id="headerOutline">pens to friends</h1>
      </div>

      <div class="container">
        <div class="line"></div>
        <div class="spreadingSmiles">
          <h2>Spreading smiles, one letter at a time</h2>
          <img src="/paper-aeroplane.svg" alt="">
        </div>
      </div>

      <div class="background_rectangle"></div>
      <img id="landingPageLogo" src="landing-page-logo.svg" alt="" width="650">
      <img id="backgroundCircle" src="/background-circle.svg" alt="">
    </div>
  </section>
</template>

<style scoped>
.headers {
  position: absolute;
  left: 260px;
  top: 100px;
}

.container {
  display: flex;
  flex-direction: column;
  position: absolute;
  left: 138px;
  top: 620px;
}

.spreadingSmiles {
  display: flex;
  flex-direction: row;
  z-index: 3;
}

.line {
  position: absolute;
  width: 434px;
  height: 0px;
  border: 5px solid #C8C8A9;
}

#headerOutline {
  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 128px;
  line-height: 50px;
  display: flex;
  align-items: center;
  text-align: center;
  color: transparent;
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: #A5A988;
}

h1 {
  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 128px;
  line-height: 50px;
  display: flex;
  align-items: center;
  text-align: center;
  color: #A5A988;
  z-index: 2;
}

h2 {
  font-family: 'Montserrat', sans-sserif;
  font-style: normal;
  font-weight: 400;
  font-size: 64px;
  line-height: 115px;
  color: #35312B;
  width: 611px;
  height: 200px;
}

#backgroundCircle {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
}

#landingPageLogo {
  position: absolute;
  bottom: 0;
  right: 0;
}

.background_rectangle {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: #C8C8A9;
  opacity: 40%;
  z-index: -1;
  border: 1rem solid white;
}

.container__landingSection {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  width: 100vw;
  height: 100vh;
}

.text__landingSection-header {
  font-size: 50px;
  font-weight: 600;
  font-family: 'Montserrat', sans-serif;
  letter-spacing: 0.02rem;
  text-align: center;
}

.text__landingSection-subheader {
  font-size: 28px;
  font-family: 'Montserrat', sans-serif;
  font-weight: 400;
  letter-spacing: 0.02rem;
  text-align: center;
}

.text__landingSection-content {
  font-size: 16px;
  font-family: 'Open Sans', sans-serif;
  max-width: 50rem;
}

@media only screen and (min-width: 320px) and (max-width: 480px) {
  .text__landingSection-header {
    font-size: 30px;
  }

  .text__landingSection-subheader {
    font-size: 20px;
  }

  .text__landingSection-content {
    font-size: 14px;
  }
}
</style>
