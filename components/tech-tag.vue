<template>
  <div class="tech-tag">
    <img style="width:20px;" :src="imageUrl" :alt="`${tech} icon`">
    {{ tech.charAt(0).toUpperCase() }}{{ tech.slice(1) }}
  </div>
</template>

<script setup>

const props = defineProps({
  tech: {
    type: String,
    required: true
  }
})

const getImageUrl = () => new URL(`../assets/images/${props.tech}.svg`, import.meta.url).href

const imageUrl = ref()

onMounted(() => {
  updateImageSrc()
})

function updateImageSrc () {
  imageUrl.value = getImageUrl()
}

</script>

<style scoped>
img{
  margin-right: auto;
}
.tech-tag{
  display: flex;
  gap:5px;
  align-items: center;
  background-color: rgb(27, 27, 27);
  border-radius: 10px;
  padding: 5px;
  border: 1px solid rgb(43, 43, 43);
  width: fit-content;
}
</style>
