<template>
  <h2>Special Opportunities</h2>
  <Carousel class="carousel" :autoplay="2000">
    <Slide v-for="(slide, index) in slides" :key="index">
      <div class="carousel-item">
        <OpportunityCard v-if="slide.header" :header="slide.header" :img="slide.img" :description="slide.description"
          :link="slide.link" />
        <div v-else class="stayTuned carousel-item">
          <h3>{{ slide.message }}</h3>
        </div>
      </div>
    </Slide>

    <template #addons>
      <Navigation />
      <Pagination />
    </template>
  </Carousel>
</template>

<script>
import { defineComponent } from 'vue'
import { Carousel, Navigation, Pagination, Slide } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
  name: 'SpecialOpportunities',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  data() {
    return {
      slides: [
        {
          header: 'Happy Hearts Indonesia',
          img: 'happyhearts.jpg',
          description: 'Happy Hearts Indonesia works with schools in low-income communities to ensure that students can attend a safe school. Happy Hearts uses its funding to build schools and provide educational resources to children in Indonesia.',
          link: 'https://www.instagram.com/p/CtZMwgmt38J/',
        },
        {
          message: 'More opportunities to come... stay tuned!',
        },
      ],
    }
  },
})
</script>

<style scoped>
.carousel {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.carousel-item {
  min-height: 200px;
  width: fit-content;
  font-size: 20px;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel-item img {
  max-width: 100%;
  height: auto;
}

.stayTuned {
  width: 26rem;
  height: 35rem;
  background-color: #fff;
  border-radius: 1rem;
  box-shadow: 0 0.2rem 0.45rem rgba(0, 0, 0, 0.1);
  padding: 0.2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

h3 {
  color: #35312b;
  text-align: center;
  font-size: 1.5rem;
  font-family: 'Montserrat', sans-serif;
  font-weight: 600;
  margin-top: 1rem;
  width: 20rem;
  letter-spacing: 0.02rem;
  line-height: 2.25rem;
}

h2 {
        font-family: 'Montserrat', sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 3rem;
        line-height: 3.6875rem;
        color: #35312b;
        margin-top: 6rem;
      }
</style>
