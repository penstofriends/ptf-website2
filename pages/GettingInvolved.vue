<template>
  <div class="container__components-gettingInvolved">
    <h1 class="text-header">Spread the Joy</h1>
    <p class="text__gettingInvolved-description">
      Pens to Friends offers two forms of letter writing for volunteers. Read
      about them below:
    </p>
    <div class="container__gettingInvolved-text">
      <div class="container__gettingInvolved-virtual">
        <h2 class="text-subheader">Virtual Letters</h2>
        <div class="container__gettingInvolved-virtual-descriptions">
          <p class="text-description">
            As we want to provide a more consistent alternative volunteering
            option , we've decided to launch “Letters of the Month.” Through
            this program, volunteers will be able to write encouraging and
            uplifting letters to Individuals that have signed up through PTF!
            These letters will be sent out within the first week of each month.
            You can write about your interests, words of encouragement, or even
            advice. Artwork will be accepted as a form of letters. Volunteers
            will be asked to submit their letters by the 25th of each month so
            that it allows our team to match letters up to recipients. Please
            keep in mind that these letters need to be appropriate!
          </p>
          <p class="text-description">
            To get started, click the link below. Please be aware that each time
            you wish to volunteer, you will have to fill out the form again. If
            you do not sign the form before submitting your letters, you will
            not receive your hours. If you have any questions, please feel free
            to dm or email our team! Thank you all for your patience as we work
            to implement this new system.
          </p>
        </div>
        <div class="container__gettingInvolved-buttons">
          <div class="container__gettingInvolved-buttons-send">
            <img
              alt="logo"
              class="logo"
              src="/sendLetter.svg"
              width="135"
              height="135"
            />
            <FormButton text="Send Letter(s)" />
          </div>
          <div class="container__gettingInvolved-buttons-recieve">
            <img
              alt="logo"
              class="logo"
              src="/receiveLetter.svg"
              width="135"
              height="135"
            />
            <FormButton text="Receive Letter(s)" />
          </div>
        </div>
      </div>

      <div class="container__gettingInvolved-physical">
        <h2 class="text-subheader">Handwritten/Physical Letters</h2>
        <p class="text-description">
          [description about physical letters] Lorem ipsum dolor sit amet,
          consectetur adipiscing elit. Sed auctor odio in massa commodo commodo.
          Integer euismod posuere ipsum eget sollicitudin. Ut commodo euismod
          urna, a lacinia arcu maximus sit amet. Etiam et sapien sed odio
          consequat consectetur at nec magna. Morbi pellentesque, mi nec finibus
          dignissim, elit ante faucibus ante, in malesuada eros lectus ac purus.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
section {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

button {
  color: #fff;
  font-size: 1rem;
  font-family: "Open Sans", sans-serif;
  font-weight: 500;
  letter-spacing: 0.05rem;
}

.text__gettingInvolved-description {
  color: #35312b;
  font-size: 1.25rem;
  font-family: "Open Sans", sans-serif;
  display: flex;
  flex-direction: column;
  flex-shrink: 0;
  text-align: center;
  margin: 2rem;
}

.container__components-gettingInvolved {
  height: 100%;
}

.container__gettingInvolved-text::before {
  content: "";
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 0.0625rem;
  height: 42rem;
  background-color: #35312b;
}

.text-header {
  color: #35312b;
  font-size: 3rem;
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  text-align: center;
  margin-top: 3rem;
}

.text-subheader {
  text-align: center;
  color: #35312b;
  font-size: 2.25rem;
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  line-height: 100%;
  margin-bottom: 0;
}

.text-description {
  color: #35312b;
  font-size: 1rem;
  font-family: "Open Sans", sans-serif;
  display: flex;
  width: 42.625rem;
  flex-direction: column;
  flex-shrink: 0;
  text-indent: 3rem;
  line-height: 1.5rem;
}

.container__gettingInvolved-text {
  display: flex;
  position: relative;
}

.container__gettingInvolved-letters {
  width: 50%;
  padding: 1rem;
  margin: 1rem;
}

.container__gettingInvolved-virtual,
.container__gettingInvolved-physical {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
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
  width: 11.5rem;
  height: 2.5rem;
  flex-shrink: 0;
  border-radius: 50px;
  background: #a5a988;
}

.container__gettingInvolved-buttons {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.container__gettingInvolved-virtual-descriptions {
  height: auto;
  display: flex;
  flex-direction: column;
}

@media only screen and (max-width: 720px) {
  section {
    text-align: center;
  }

  .text-subheader {
    width: 20rem;
    text-align: center;
    overflow-wrap: normal;
    word-break: break-all;
    font-size: 2rem;
  }

  .container__gettingInvolved-text::before {
    display: none;
  }

  .container__gettingInvolved-text {
    flex-direction: column;
    align-items: center;
  }

  .container__gettingInvolved-letters {
    width: 100%;
    padding: 1rem;
    margin: 1rem;
  }

  .container__gettingInvolved-buttons-send,
  .container__gettingInvolved-buttons-recieve {
    margin: 1rem;
  }
  .container__gettingInvolved-buttons-send button,
  .container__gettingInvolved-buttons-recieve button {
    margin-top: 1rem;
    width: 8rem;
    height: 3rem;
    font-size: 1rem;
  }

  .container__gettingInvolved-buttons-recieve img,
  .container__gettingInvolved-buttons-send img {
    width: 6rem;
  }

  .text-description {
    width: 80vw;
    height: auto;
    margin-top: 1rem;
  }
}
@media only screen and (min-width: 721px) and (max-width: 1200px) {
  .text-header {
    font-size: 4rem;
    margin-bottom: 0;
  }
  .container__gettingInvolved-text {
    flex-direction: column;
  }
  .container__gettingInvolved-text::before {
    display: none;
  }
  .container__gettingInvolved-physical {
    padding-bottom: 10%;
  }
  .text-description {
    width: 90vw;
  }
}
</style>
