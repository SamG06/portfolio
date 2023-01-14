<template>
  <div>
    <img class="pfp" src="~/assets/images/pfp.png" alt="profile picture">
  </div>
</template>

<script lang="ts" setup>

</script>

<style scoped>
img{
  width: 95px;
  border-radius: 15%;
  filter: grayscale(.5);
  transition: filter .2s, transform .2s;
  cursor: pointer;
}

img:hover{
  filter: grayscale(0);
  transform: rotate(-2deg);
}
</style>
