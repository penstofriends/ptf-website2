<template>
  <div class="faq-item">
    <div class="faq-question" @click="toggleAnswer(); console.log(question, answer, isVisible)">
      <h3>{{ question }}</h3>
      <span class="faq-toggle">{{ isVisible }}</span>
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
  isVisible = !isVisible
}
</script>

<style>
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
}

.faq-toggle {
  margin-left: auto;
  font-size: 16px;
}

.faq-answer {
  margin-top: 10px;
  padding: 10px;
}
</style>
