<template>
  <section id="section__SpecialOpportunities">
    <h2>Special Opportunities</h2>
    <Carousel class="carousel" :items-to-show="1">
      <Slide v-for="(slide, index) in slides" :key="index">
          <OpportunityCard v-if="slide.header" :header="slide.header" :img="slide.img" :description="slide.description"
            :link="slide.link" />
          <OpportunityCard v-else :description="slide.message"/>
      </Slide>

      <template #addons>
        <Navigation />
        <Pagination />
      </template>
    </Carousel>
  </section>
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
      settings: {
        itemsToShow: 1,
        snapAlign: 'center',
      },
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
#section__SpecialOpportunities {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100vw;
}
.carousel-item img {
  max-width: 100%;
  height: auto;
}
.carousel {
  width: 40vw;
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

.carousel__pagination{
  padding: 0;
  margin: 0;
}


@media only screen and (min-width: 320px) and (max-width: 480px) {
  .stayTuned {
    width: 21rem;
    height: 35rem;
  }

  h2 {
    font-size: 2.5rem;
    width: 100vw;
    text-align: center;

  }

  .carousel {
    width: 100vw;
  }
  .carousel__next {
    display: none;
  }
}
</style>
