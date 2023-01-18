<template>
  <main class="intro">
    <div class="meta-info-box">
      <DynamicPfp />
      <div>
        <p>Name: Samuel</p>
        <p>Age: {{ age }}</p>
        <p>Based In: United States 🇺🇸</p>
      </div>
    </div>
    <div class="link-drawer">
      <a class="link github-link" href="https://github.com/SamG06" target="_blank" rel="noopener noreferrer"><img src="~/assets/images/github-mark-white.svg" alt="github logo"></a>
      <a class="link contact-link" href="mailto:the.dev.sam@pm.me"><img src="~/assets/images/at-the-rate-icon.svg" alt="email logo"></a>
    </div>
    <div class="intro-text">
      <h2>Uh...hi?</h2>
      <p>
        I'm a web developer with experience in languages such as JavaScript, Python (Django).
        I have become particularly interested in
        <LinkHoverPreview class="vue-link" hyper-link="https://vuejs.org/" image-url="vue-placeholder.webp" url-text="Vue's Main Site" link-name="Vue" /> &
        <LinkHoverPreview class="go-link" hyper-link="https://go.dev/" image-url="golang-placeholder.png" url-text="Go's Main Site" link-name="Go" /> recently, and love to explore new tools as I have always done throughout my career.
        I take pride in my adaptability and ability to thrive in diverse environments. My main goal is to continue  expanding my skills as a developer so I'm always up for new challenges!
      </p>
    </div>
  </main>
</template>

<script setup>
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
h2{
    margin-bottom: .5em;
    margin-top: .5em;
}
  .meta-info-box{
    display: flex;
  }

  .intro-text{
    margin-top: 2em;
  }
  .meta-info-box div{
    margin-right: 10px;
  }

  .link-drawer{
    display: flex;
  }

  .link-drawer{
    background-color: #333b40;
    width: fit-content;
    border-radius: 5px;
    margin-top: 10px;
  }
  .link {
    color: white;
    padding:10px;
    margin-top: 10px;
    display: block;
  }

  .link img{
    width: 20px;
  }
</style>
