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
    <img src="https://placekitten.com/g/500/300" alt="cat placeholder">
    Text here or something
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
  }
})

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
    display: none;
    touch-action: none;
    pointer-events: none;
    position: fixed;
    transform: translateY(30px);
    width:90%;
    max-width: 200px;
    transition: opacity .2s;
  }

  .preview-box img{
    width:100%;
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
