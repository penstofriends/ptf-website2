<template>
  <div class="faq-item">
    <div class="faq-question" @click="toggleAnswer">
      <h3>{{ question }}</h3>
      <span class="faq-toggle">{{ isVisible ? '-' : '+' }}</span>
    </div>
    <div class="faq-answer" v-show="isVisible">
      {{ answer }}
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
let isVisible = ref(false)

defineProps({
  question: {
    type: String,
    required: true
  },
  answer: {
    type: String,
    required: true
  },
})

function toggleAnswer() {
  isVisible.value = !isVisible.value
}
</script>

<style scoped>
.faq-question {
  display: flex;
  cursor: pointer;
  padding: 0.1rem;
  background-color: white;
}

.faq-question h3 {
  margin: 0;
  font-size: 20px;
}

.faq-question {
  max-width: 75rem;
  padding: 0.5rem;
  color: #35312B;
  font-size: 1rem;
  font-family: 'Open Sans', sans-serif;
  font-weight: 600;
}

.faq-toggle {
  margin-left: auto;
  font-size: 16px;
}

.faq-answer {
  margin-top: 10px;
  padding: 10px;
  max-width: 75rem;
  padding: 0.5rem;
  color: #35312B;
  font-size: 1.25rem;
  font-family: 'Open Sans', sans-serif;
  font-weight: 400;
}
</style>
