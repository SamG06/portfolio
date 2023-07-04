!!<template>
  <div class="theme-circles-section">
    <div class="circle color-purple" @click="themeChange('purple-theme')" />
    <div class="circle color-blue" @click="themeChange('blue-theme')" />
    <div class="circle color-green" @click="themeChange('green-theme')" />
  </div>
</template>

<script setup>

const currentTheme = ref('purple-theme')

function themeChange (theme) {
  document.documentElement.classList.replace(currentTheme.value, theme)
  currentTheme.value = theme
}

onMounted(() => {
  document.documentElement.classList.add(currentTheme.value)
})

</script>

<style scoped>
.theme-circles-section{
    display: flex;
    gap:10px;
    margin-right: 10px;
    position: absolute;
    right:0;
    top:50%;
    transform: translateY(-50%);
}
.circle{
    background-color: #ffffff;
    border-radius: 5px;
    width: 30px;
    height: 30px;
    transition: transform .2s;
    cursor: pointer;
}

.circle:hover{
    transform: scale(1.3);
}

.color-blue{
    background-color: #8eaaff;
}

.color-green{
    background-color: #cbff8e;
}

.color-purple{
    background-color: #a389ee;
}
</style>
