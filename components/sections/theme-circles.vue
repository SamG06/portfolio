!!<template>
  <div class="theme-circles-section">
    <div class="circle color-blue" />
    <div class="circle color-green" />
    <div class="circle color-purple" />
  </div>
</template>

<script setup>

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
    border-radius: 100%;
    width: 30px;
    height: 30px;
    transition: transform .2s;
    cursor: pointer;
}

.circle:hover{
    transform: scale(1.5);
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
