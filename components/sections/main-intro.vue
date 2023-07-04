<template>
  <main class="intro">
    <div class="left-side">
      <div class="meta-info-box">
        <div>
          <h1>
            Samuel Graham
          </h1>
        </div>
      </div>
      <div class="intro-text">
        <p> JavaScript/Python Developer based in the United States.</p>
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
