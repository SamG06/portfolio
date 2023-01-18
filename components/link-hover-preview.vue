<template>
  <a
    ref="linkArea"
    v-bind="$attrs"
    :href="props.hyperLink"
    target="_blank"
    rel="noopener noreferrer"
    @mouseenter="showPreview"
    @mouseleave="hidePreview"
    @focusin="showPreview"
    @focusout="hidePreview"
  > {{ props.linkName }}</a>
  <span ref="previewBox" class="preview-box">
    <img :src="imageUrl" alt="placeholder">
    {{ imageUrl }}
    <p>{{ urlText }}</p>
  </span>
</template>

<script lang="ts" setup>
const props = defineProps({
  linkName: {
    type: String,
    default: 'Link Name'
  },
  hyperLink: {
    type: String,
    default: 'https://samuelgraham.dev/'
  },
  imageUrl: {
    type: String,
    default: 'https://placekitten.com/g/500/300'
  },
  urlText: {
    type: String,
    default: 'Website Description'
  }
})

const getImageUrl = () => new URL(`../assets/images/${props.imageUrl}`, import.meta.url).href

const imageUrl = ref()

onMounted(() => {
  updateImageSrc()
})

watch(() => props.imageUrl, () => {
  updateImageSrc()
})

function updateImageSrc () {
  imageUrl.value = getImageUrl()
}

// Showing preview
const previewBox = ref<HTMLSpanElement| null>(null)
const linkArea = ref<HTMLAnchorElement| null>(null)

const showPreview = () => {
  if (!previewBox.value || !linkArea.value) { return }
  const link = linkArea.value.getBoundingClientRect()
  previewBox.value.style.cssText = `opacity:1;top:${link.top}px;bottom:${link.bottom}px;left:${link.right}px`
}

const hidePreview = () => {
  if (!previewBox.value || !linkArea.value) { return }
  previewBox.value.style.opacity = '0'
}
</script>

<style scoped>
  .preview-box{
    opacity: 0;
    touch-action: none;
    pointer-events: none;
    position: fixed;
    transform: translateY(30px);
    width:90%;
    max-width: 200px;
    transition: opacity .2s;
    background-color: #272727;
    height: fit-content;
    border-radius: 10px;
    overflow: hidden;
    padding:10px;
    font-size: 0.8em;
  }

  .preview-box img{
    width:100%;
    height: 130px;
    object-fit:cover;
  }

  .showing{
    opacity: 1;
  }

  a{
    text-decoration: none;
    transition: transform .2s;
    display: inline-block;
  }
  .vue-link{
      color: var(--vue-bg);
    }

  .vue-link:hover{
    color: #65d2a1;
    transform: scale(1.1);
  }

  .go-link{
    color: var(--go-bg);
  }

  .go-link:hover{
    color: #7dcbef;
    transform: scale(1.1);
  }
</style>
