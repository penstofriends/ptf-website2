<template>
    <div class="card">
      <img :src="img" alt="Card Image" class="card-image">
      <h2 class="card-header">{{ header }}</h2>
      <p class="card-description">{{ description }}</p>
  
      <a :href="link" target="_blank" rel="noopener">
        <button class="card-button">Learn More</button>
      </a>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      header: {
        type: String,
        required: true
      },
      img: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      },
      link: {
        type: String,
        required: true
      }
    }
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
    color: #35312B;
    text-align: center;
    font-size: 1.5rem;
    font-family: 'Montserrat', sans-serif;
    font-weight: 600;
    margin-top: 1rem;
  }
  
  .card-description {
    margin-top: 0.25rem;
    color: #35312B;
    font-size: 1rem;
    font-family: 'Open Sans', sans-serif;
    width: 20rem;
    text-align: center;
  }
  
  .card-button {
    margin-top: 0.2rem;
    padding: 0.5rem 1rem;
    background-color: #A5A988;
    color: #fff;
    border: none;
    border-radius: 0.25rem;
    cursor: pointer;
    text-decoration: none; 
    font-family: 'Open Sans', sans-serif;
    font-size: 1rem;
  }
  </style>
  