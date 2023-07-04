<template>
  <nav>
    <div class="links-container">
      <div class="links">
        <a onclick="scrollToAnchor('home')">HOME</a>
        <a onclick="scrollToAnchor('about')">ABOUT</a>
        <a onclick="scrollToAnchor('projects')">PROJECTS</a>
      </div>
      <ThemeCircles />
    </div>
  </nav>
</template>

<script setup>
import ThemeCircles from './theme-circles.vue'

</script>

<style scoped>
nav {
    width: 100%;
    height: 50px;
    display: flex;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    align-items: center;
    position: fixed;
    top: 0;
    background-color: #202020;
    z-index: 500;
    display: flex;
    justify-content: center;
    height: 60px;
    user-select: none;
    padding-left: 30px;
}
a {
    cursor: pointer;
    color: var(--light-text);
}
.links-container {
    max-width: 1050px;
    width: 100%;
    position: relative;
}

.links {
    display: block;
}

.links {
    display: flex;
}
.links a {
    display: block;
    margin-left: 15px;
    font-size: 16px;
}
.links a:first-child {
    margin-left: 0px;
}

.links a:hover {
    transform: scale(1.1);
    color: #ae98f0;
}

.links a:active {
    transform: scale(1);
}

</style>
