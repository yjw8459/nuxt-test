<script lang="ts" setup>
import _ from 'lodash'
const wheelEvent = (event: any) => {
    console.log('wheel');
    
}
onMounted(() => {
    console.log('test');
    document.addEventListener('wheel', _.throttle(wheelEvent, 1000));
})
</script>
<template>
<div>
    <div class="container" style="background-color: red;"></div>
    <div class="container" style="background-color: tomato;"></div>
    <div class="container" style="background-color: aqua;"></div>
</div>
</template>
<style>
.container {
    height: 100vh;
    width: 100%;
}
</style>