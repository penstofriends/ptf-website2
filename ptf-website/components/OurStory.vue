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
      <img src="/our-story-graphic.svg"
        alt="letter with the words, 'dear friend'. the letter is surrounded by fish graphics">
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
  height: 70vh;
  padding-left: 5vw;
}

.left {
  display: flex;
  flex-direction: column;
  width: 50vw;
  padding: 0 1.5rem 0 1.5rem;
}

.right img {
  width: 45vw;
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
  margin-bottom: 1rem;
}

p {
  text-indent: 4rem;
  font-family: 'Open Sans', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 1rem;
  line-height: 1.625rem;
  display: flex;
  align-items: center;
  color: #35312B;
  width: 45vw;
}

@media only screen and (max-width: 480px) {
  #section__ourStory {
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100vw;
    height: auto;
    padding: 0;
  }

  .left {
    order: 2;
    text-align: left;
  }

  .right {
    order: 1;
  }

  .right img {
    width: 28rem;
  }

  h2 {
    font-size: 2.5rem;
    line-height: 3rem;
    margin-top: 0;
    text-align: center;
    width: 100vw;
  }

  p {
    width: 100%;
    height: auto;
    margin-top: 0;
    font-size: 1rem;
    line-height: 1.5rem;
  }
}
</style>
