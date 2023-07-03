<template>
  <main class="intro">
    <div class="left-side">
      <div class="meta-info-box">
        <div>
          <h1>
            Samuel Graham
            {{ age }}
          </h1>
        </div>
      </div>
      <div class="intro-text">
        <p> JavaScript/Python Developer based in the United States.</p>
        <!-- <p>
          I'm a web developer with experience in languages such as JavaScript, Python (Django).
          I have become particularly interested in
          <LinkHoverPreview class="vue-link" hyper-link="https://vuejs.org/" image-url="vue-placeholder.webp" url-text="Vue's Main Site" link-name="Vue" /> &
          <LinkHoverPreview class="go-link" hyper-link="https://go.dev/" image-url="golang-placeholder.png" url-text="Go's Main Site" link-name="Go" /> recently, and love to explore new tools as I have always done throughout my career.
          I take pride in my adaptability and ability to thrive in diverse environments. My main goal is to continue  expanding my skills as a developer so I'm always up for new challenges!
        </p> -->
      </div>
      <div class="intro-buttons">
        <a href="https://github.com/SamG06" target="_blank" rel="noopener noreferrer">About Me</a>
        <a href="https://github.com/SamG06" target="_blank" rel="noopener noreferrer">My Github</a>
      </div>
    </div>
    <TerminalWindow class="terminal-intro" />
  </main>
</template>

<script setup>
import TerminalWindow from '../terminal-window.vue'
</script>

<style scoped>
h1{
  font-size: 2.5em;
}
main{
  display: flex;
}
.left-side{
  width: 50%;
  align-self: flex-start;
}

.terminal-intro{
  margin-left: auto;
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
