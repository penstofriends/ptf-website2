<template>
  <div class="container__topArrow none-topArrow">
    <a href="#landing-section" class="anchor__topArrow">
      <p href="#section__landingSection" class="icon__topArrow"></p>
    </a>
  </div>
</template>

<script setup>
const showArrow = ref(false)
const route = useRoute()
function ifScrolledEnough() {
  const topArrow = document.querySelector('.container__topArrow')

  if (route.path == '/') {
    if (window.scrollY > 300) {
      showArrow.value = true
      topArrow.classList.add('show-topArrow')
      topArrow.classList.remove('none-topArrow')

      topArrow.classList.remove('pop-out')
      topArrow.classList.add('pop-in')
    } else if (window.screenY < 300 && showArrow.value == true && useRoute().path == '/') {
      topArrow.classList.remove('show-topArrow')
      topArrow.classList.add('none-topArrow')

      topArrow.classList.add('pop-out')
      topArrow.classList.remove('pop-in')
    }
  }
}

onMounted(() => {
  window.addEventListener('scroll', ifScrolledEnough)
})
</script>

<style scoped>
.container__topArrow {
  height: 60px;
  width: 60px;
  opacity: 0.7;

  position: fixed;
  bottom: 1%;
  right: 2%;

  background-color: white;

  border: 2px solid #A5A988;
  border-radius: 20%;

  z-index: 2;
}

.icon__topArrow {
  border: 1px solid #A5A988;
  border-width: 0 5px 5px 0;
  display: inline-block;
  padding: 10px;

  transform: rotate(-135deg);
  -webkit-transform: rotate(-135deg);
}

.anchor__topArrow {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 100%;
  height: 100%;
  padding-top: 5px;
}

.show-topArrow {
  opacity: 1;
}

.none-topArrow {
  opacity: 0;
}

.pop-in {
  animation: pop-in 1s;
}

.pop-out {
  animation: pop-out 1s;
}

@keyframes pop-in {
  from {
    opacity: 0;
    transform: translatey(150px);
  }

  to {
    opacity: 1;
    transform: translatey(0);
  }
}

@keyframes pop-out {
  from {
    opacity: 1;
    transform: translatey(0);
  }


  to {
    opacity: 0;
    transform: translatey(150px);
  }
}
</style>

