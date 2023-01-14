<template>
  <main>
    <section class="intro">
      <div class="meta-info-box">
        <DynamicPfp />
        <div>
          <p>Name: Samuel</p>
          <p>Age: {{ age }}</p>
        </div>
      </div>
      <div class="link-drawer">
        <a class="contact-button" href="mailto:the.dev.sam@pm.me"><img src="~/assets/images/github-mark-white.svg" alt="github logo"></a>
        <a class="contact-button" href="mailto:the.dev.sam@pm.me"><img src="~/assets/images/at-the-rate-icon.svg" alt="email logo"></a>
      </div>

      <h1>Uh...hi?</h1>
      <p>
        I'm a web developer with experience in languages such as JavaScript, Python, and Django.
        I have become particularly interested in
        <LinkHoverPreview class="vue-link" hyper-link="https://vuejs.org//" link-name="Vue" /> &
        <LinkHoverPreview class="go-link" hyper-link="https://go.dev/" link-name="Go" /> recently, and love to explore new tools as I have always done throughout my career.
        I take pride in my adaptability and ability to thrive in diverse environments. My main goal is to continue  expanding my skills as a developer so I'm always up for new challenges!
      </p>
    </section>
    <section>
      <div>
        <h2>Career</h2>
        <hr>
        <div>
          <h3>Blockbuster Costumes Jan 2022 - Present Day</h3>
          <p>
            - Tech Stack: Python/Django, Bootstrap, Jquery, JavaScript, Vue
          </p>
        </div>
      </div>
    </section>
  </main>
</template>

<script lang="ts" setup>
import LinkHoverPreview from '~~/components/link-hover-preview.vue'

const age = computed(() => {
  const today = new Date()
  const myBirthday = new Date('1999/08/06')
  let myAge = today.getFullYear() - myBirthday.getFullYear()
  const m = today.getMonth() - myBirthday.getMonth()
  if (m < 0 || (m === 0 && today.getDate() < myBirthday.getDate())) {
    myAge -= 1
  }

  if (myAge > 100) {
    return `${myAge} (Am I still alive...o.O?)`
  }
  return myAge
})
</script>

<style scoped>
  main{
    display: flex;
    flex-flow: column;
    align-items: center;
    justify-content: center;
    margin-top: 30px;
  }

  h3{
    font-weight: 400;
  }

  section{
    width:90%;
    max-width: 900px;
  }

  p{
    color: #bbbbbb;
    line-height: 25px;
  }

  a{
    text-decoration: none;
  }

  .link-drawer{
    display: flex;
  }
  .meta-info-box{
    display: flex;

  }

  .meta-info-box div{
    margin-right: 10px;
  }
  .meta-info-box p{
    line-height: 10px;
  }

  .link-drawer{
    background-color: #333b40;
    width: fit-content;
    border-radius: 5px;
    margin-top: 10px;
  }
  .contact-button{
    color: white;
    padding:10px;
    margin-top: 10px;
    display: block;
  }

  .contact-button img{
    width: 20px;
  }
</style>
