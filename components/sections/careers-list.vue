<template>
  <section>
    <div>
      <h2>Career</h2>

      <div class="career-card">
        <h3>Blockbuster Costumes Jan 2022 - Present Day</h3>
        <p>Help craft proprietary warehouse solutions increasing productivity.</p>
        <p>
          - Tech Stack: <TechTag tech="vue" />, <TechTag tech="python" />, Postgres, Bootstrap, JavaScript ES6
        </p>
      </div>

      <div class="career-card">
        <h3>IBM Internship June 2016 - August 2016 </h3>
        <p>Created a </p>
        <p>
          - Tech Stack: React, PHP, MySQL
        </p>
      </div>
    </div>
  </section>
</template>

<script setup>
import TechTag from '../tech-tag.vue'

</script>

<style scoped>
h2{
  margin-bottom: 20px;
}
h3{
  margin-bottom: 10px;
}
.career-card{
  background-color: rgb(22, 22, 22);
  padding: 20px;
  border-radius: 10px;;
}
</style>
