<template>
  <div class="card">
    <img v-if="img" :src="img" alt="Card Image" class="card-image" />
    <h2 v-if="header" class="card-header">{{ header }}</h2>
    <p v-if="description" class="card-description">{{ description }}</p>

    <a v-if="header" :href="link" target="_blank" rel="noopener">
      <button class="card-button">Learn More</button>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    header: {
      type: String,
    },
    img: {
      type: String,
    },
    description: {
      type: String,
    },
    link: {
      type: String,
    },
  },
};
</script>

<style scoped>
.card {
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

.card-image {
  width: 20rem;
  height: auto;
  border-radius: 0.75rem;
}

.card-header {
  color: #35312b;
  text-align: center;
  font-size: 1.5rem;
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  margin-top: 1rem;
}

.card-description {
  margin-top: 0.25rem;
  color: #35312b;
  font-size: 1rem;
  font-family: "Open Sans", sans-serif;
  width: 20rem;
  text-align: center;
}

.card-button {
  margin-top: 0.2rem;
  padding: 0.5rem 1rem;
  background-color: #a5a988;
  color: #fff;
  border: none;
  border-radius: 0.25rem;
  cursor: pointer;
  text-decoration: none;
  font-family: "Open Sans", sans-serif;
  font-size: 1rem;
}

@media only screen and (max-width: 720px) {
  .card {
    width: 21rem;
    height: 35rem;
  }

  .card-image {
    width: 17rem;
    margin-top: 0.8rem;
  }
  .card-header {
    color: #35312b;
    text-align: center;
    font-size: 1.4rem;
    font-family: "Montserrat", sans-serif;
    font-weight: 600;
    margin-top: 1rem;
  }

  .card-description {
    margin-top: 0.25rem;
    color: #35312b;
    font-size: 1rem;
    font-family: "Open Sans", sans-serif;
    width: 16rem;
    text-align: center;
  }

  .card-button {
    margin-top: 0.2rem;
    font-size: 1rem;
  }
}

@media only screen and (min-width: 721px) and (max-width: 1200px) {
  .card {
    width: 35rem;
    height: 50rem;
  }
  .card-image {
    width: 30rem;
  }
  .card-header {
    font-size: 2rem;
  }
  .card-description {
    width: 80%;
    font-size: 1.5rem;
  }
}
</style>
