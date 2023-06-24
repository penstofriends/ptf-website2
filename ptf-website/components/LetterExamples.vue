<template>
  <section id="section__letterExamples">
    <div class="container__line">
      <div id="container__line-inner"></div>
    </div>
    <div class="container__letterExamples">
      <div class="container__letterExamples-pictures">
        <img src="/letteronplants.jpg" class="image__hidden" />
        <img src="/moreorigamifroggylmao.jpg" class="image__hidden" />
        <img src="/pinkletter.jpg" class="image__hidden" />
        <img src="/SOCUTE.jpg" class="image__hidden" />
        <img src="/bnw.jpg" class="image__hidden" />
        <img src="/yeah.jpg" class="image__hidden" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('image__visible')
        }
      })
    })

    const hiddenElements = document.querySelectorAll('.image__hidden')
    hiddenElements.forEach((element) => {
      observer.observe(element)
    })
  }
}
</script>

<style scoped>

#container__line-inner {
  width: 100vw;
  border: 5px solid #A5A988;
  margin: 1rem auto;
  display: flex;
  align-items: center;
  justify-content: center;
}

#section__letterExamples {
  width: 100vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

img {
  height: 22rem;
  margin: 1.2rem;
}

.container__letterExamples-pictures {
  display: flex;
  flex-direction: row;
  justify-content: center;
  padding: 1rem;
  background-color: #A5A988;
}


/* hidden images will be invisible until intersected by the observer, and then will be visible with a transition of coming from the left staggered */
.image__hidden {
  opacity: 0;
  filter: blur(5px);
  transform: translateX(-100%);
  transition: all 1s;
}

.image__visible {
  opacity: 1;
  filter: blur(0);
  transform: translateX(0);
}

/* staggered transition */
.image__visible:nth-child(1) {
  transition-delay: 0.1s;
}

.image__visible:nth-child(2) {
  transition-delay: 0.3s;
}

.image__visible:nth-child(3) {
  transition-delay: 0.5s;
}

.image__visible:nth-child(4) {
  transition-delay: 0.7s;
}

.image__visible:nth-child(5) {
  transition-delay: 0.9s;
}

.image__visible:nth-child(6) {
  transition-delay: 1.1s;
}


@media only screen and (min-width: 320px) and (max-width: 480px) {
  .container__letterExamples-pictures {
    flex-direction: column;
  }

  .image__visible:nth-child(1) {
    transition-delay: 0.1s;
  }

  .image__visible:nth-child(2) {
    transition-delay: 0.1s;
  }

  .image__visible:nth-child(3) {
    transition-delay: 0.1s;
  }

  .image__visible:nth-child(4) {
    transition-delay: 0.1s;
  }
}
</style>


