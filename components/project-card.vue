<template>
  <article>
    <h2>{{ projectName }}</h2>
    <p>{{ projectDesc }}</p>
  </article>
</template>

<script setup>
defineProps({
  projectName: {
    type: String,
    default: 'Project Name'
  },
  projectDesc: {
    type: String,
    default: 'Default content description'
  }

})
</script>

<style scoped></style>
