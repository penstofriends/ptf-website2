<template>
  <div class="container__components-gettingInvolved">
    <h1 class="text-header">Spread the Joy</h1>


    <div class="container__gettingInvolved-text">
      <div class="container__gettingInvolved-virtual container__gettingInvolved-letters">

        <h2 class="text-subheader">Virtual Letters</h2>
        <p class="text-description">
          [description about virtual letters] Lorem ipsum dolor sit amet, consectetur adipiscing
          elit. Sed auctor odio in massa commodo commodo. Integer euismod posuere ipsum eget
          sollicitudin. Ut commodo euismod urna, a lacinia arcu maximus sit amet. Etiam et sapien
          sed odio consequat consectetur at nec magna. Morbi pellentesque, mi nec finibus dignissim,
          elit ante faucibus ante, in malesuada eros lectus ac purus.

        </p>
        <div class="container__gettingInvolved-buttons">
          <div class="container__gettingInvolved-buttons-send">

            <img alt="logo" class="logo" src="/sendLetter.svg" width="135" height="135" />
            <FormButton text="Send Letter(s)" />

          </div>
          <div class="container__gettingInvolved-buttons-recieve">

            <img alt="logo" class="logo" src="/receiveLetter.svg" width="135" height="135" />
            <FormButton text="Receive Letter(s)" />

          </div>
        </div>
      </div>

      <div class="container__gettingInvolved-physical container__gettingInvolved-letters">

        <h2 class="text-subheader">Handwritten/Physical Letters</h2>
        <p class="text-description">
          [description about physical letters] Lorem ipsum dolor sit amet, consectetur adipiscing
          elit. Sed auctor odio in massa commodo commodo. Integer euismod posuere ipsum eget
          sollicitudin. Ut commodo euismod urna, a lacinia arcu maximus sit amet. Etiam et sapien
          sed odio consequat consectetur at nec magna. Morbi pellentesque, mi nec finibus dignissim,
          elit ante faucibus ante, in malesuada eros lectus ac purus.
        </p>

      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.container__components-gettingInvolved {
  height: 100%;
}

.container__gettingInvolved-text::before {
  content: "";
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 2.5px;
  height: 100%;
  background-color: black;
}

.text-header {
  color: #000;
  font-size: 3rem;
  font-family: 'Montserrat', sans-serif;
  font-weight: 600;
  line-height: 100%;
  text-align: center;
}

.text-subheader {
  text-align: center;
  color: #000;
  font-size: 2.25rem;
  font-family: 'Montserrat', sans-serif;
  font-weight: 600;
  line-height: 100%;
}

.text-description {
  font-family: 'Noto Sans', sans-serif;
  font-weight: 400;
  font-size: 1.25rem;
  max-width: 50rem;
  text-indent: 3rem;
  margin-bottom: 2rem;
  line-height: 1.75rem;
}

.container__gettingInvolved-text {
  display: flex;
  width: 95%;
  position: relative;
}

.container__gettingInvolved-letters {
  width: 50%;
  padding: 1rem;
  margin: 1rem;
}

.container__gettingInvolved-buttons-send,
.container__gettingInvolved-buttons-recieve {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 1.5rem;
}

.container__gettingInvolved-buttons-send button,
.container__gettingInvolved-buttons-recieve button {
  margin-top: 1rem;
  width: 10.9375rem;
height: 2.375rem;
flex-shrink: 0;
border-radius: 50px;
background: #A5A988;
}

.container__gettingInvolved-buttons {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
</style>
