<template>
  <div class="content">
    <SectionsNavigationBar />
    <SectionsMainIntro />
    <SectionsAboutMe />
    <SectionsTechnologiesList />
    <SectionsCareersList />
    <SectionsProjectsList />
  </div>
</template>

<style>
  .content{
    display: flex;
    flex-flow: column;
    align-items: center;
    justify-content: center;
    margin-top: 1.8em;
    padding-bottom: 70px;
    margin-top: 200px;
  }

  h3{
    font-weight: 400;
  }

  main, section{
    width:90%;
    max-width: 1050px;
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
