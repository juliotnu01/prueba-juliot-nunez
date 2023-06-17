
<script setup >
import MainComponent from '../Maincomponent.vue'
const MainLayout = `mt-14 grid grid-cols-2 gap-4  px-6 pb-2 max-[640px]:grid-cols-1`
</script>
<template>
    <div :class="MainLayout">
       <MainComponent />
    </div>
</template>