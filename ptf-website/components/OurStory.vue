<template>
  <section id="section__ourStory">

    <div class="left">
      <h2>Our Story</h2>
      <p> In February 2021, Pens to Friends was born in a small town in Arizona, by a group of high schoolers
        who wanted to make the world a little brighter. One of our founders grew up hearing stories of her parents'
        struggles in foster care. We wanted to do something that combined our passion for art and desire to create
        positive
        change. Quickly, we grew from an organization that connected with a couple of kids to one that’s managed to spread
        light all around the world. We realize that even the smallest things can make a day brighter—a piece of art, a
        heartfelt
        story, or even just a few kind words. At Pens to Friends, our goal is to band the world together.</p>
    </div>
    <div class="right">
      <img src="/our-story-graphic.svg" alt="letter with the words, 'dear friend'. the letter is surrounded by fishies" >
    </div>
  </section>
</template>


<style scoped>
#section__ourStory {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  width: 100vw;
  height: 100vh;
  padding: 2rem;
}

.left{
  display: flex;
  flex-direction: column;
}

h2 {
  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 3rem;
  line-height: 3.6875rem;
  display: flex;
  align-items: center;
  text-align: center;
  color: #35312B;
}

p {
  text-indent: 4rem;
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 1.25rem;
  line-height: 1.875rem;
  display: flex;
  align-items: center;
  color: #35312B;
  width: 48.5rem;
  height: 15rem;
}
</style>