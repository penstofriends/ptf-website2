<template>
  <h1 class="faq__title">Questions?</h1>
  <div class="faq__description">
    <p class="faq__description-text">
      Here are a few of our most commonly asked; if the answer you're looking for is still not here,
      feel free to contact us.
    </p>
  </div>
  <div class="faq-list">
    <div class="faq-item" v-for="(FAQ, index) in FAQs" :key="index">
      <DropDown :question="FAQ.question" :answer="FAQ.answer"></DropDown>
    </div>
  </div>
</template>

<script setup>
import DropDown from '../components/DropDown.vue'
import { FAQs } from '../assets/FAQs.js'
</script>

<style scoped>
.faq__title {
  color: #35312B;
  font-size: 3rem;
  font-family: 'Montserrat', sans-serif;
  font-weight: 600;
  text-align: center;
  margin-top: 3rem;
}

.faq__description {
  color: #35312B;
  font-size: 1.25rem;
  font-family: 'Open Sans', sans-serif;
  display: flex;
  flex-direction: column;
  flex-shrink: 0;
  text-align: center;
}


.faq__description-text {
  text-indent: 0;
  text-align: center;
}

.faq-list {
  margin: 0 auto;
  max-width: 65rem;
}

.faq-item {
  margin-bottom: 20px;
  width: 100%;
}
</style>
