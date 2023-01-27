<template>
  <div class="content">
    <SectionsMainIntro />
    <SectionsTechnologiesList />
    <SectionsCareersList />
    <SectionsProjectsList />
  </div>
</template>

<script lang="ts" setup>

</script>

<style>
  .content{
    display: flex;
    flex-flow: column;
    align-items: center;
    justify-content: center;
    margin-top: 1.8em;
    padding-bottom: 70px;
  }

  h3{
    font-weight: 400;
  }

  main, section{
    width:90%;
    max-width: 900px;
    margin-top: 2em;
  }

  section{
    margin-top: 4em;
  }
  p{
    color: #d6d6d6;
    line-height: 2em;
    font-size: 1rem;
  }

  a{
    text-decoration: none;
  }
</style>
