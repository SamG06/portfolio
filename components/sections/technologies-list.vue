<template>
  <section>
    <h2>Technologies</h2>
    <ul class="technologies-list">
      <li v-for="technology in technologies" :key="technology.name">
        <a :href="technology.link" target="_blank" rel="noopener noreferrer">{{ technology.name }}</a>
      </li>
    </ul>
  </section>
</template>

<script lang="ts" setup>

interface Technology {
  name: string;
  link: string;
}

const technologies: Technology[] = [
  { name: 'HTML', link: 'https://html.spec.whatwg.org/' },
  { name: 'CSS', link: 'https://developer.mozilla.org/en-US/docs/Web/CSS' },
  { name: 'JavaScript', link: 'https://javascript.info/' },
  { name: 'Vue', link: 'https://vuejs.org/' },
  { name: 'WebRTC', link: 'https://www.w3.org/TR/webrtc/' },
  { name: 'Node', link: 'https://nodejs.org/en/' },
  { name: 'PostgreSQL', link: 'https://www.postgresql.org/' },
  { name: 'VsCode', link: 'https://code.visualstudio.com/' },
  { name: 'Pycharm', link: 'https://www.jetbrains.com/pycharm/' },
  { name: 'Docker', link: 'https://www.docker.com/' },
  { name: 'Git', link: 'https://git-scm.com/' }
]

</script>

<style scoped>
  .technologies-list{
    list-style: none;
    display: flex;
    gap: 10px;
    margin-top: 10px;
  }

  .technologies-list li{
    background-color: gray;
    padding: 10px;
    width:100%;
  }

  .technologies-list a{
    color: white;
  }

</style>
