<script setup>
import logo from '../../assets/logo.svg'
import headerComponent from '../HeaderComponent.vue'
import breadCrumbComponent from '../BreadCrumbComponent.vue'
const classLayoutHeader = `w-full h-[60px] max-h-[60px] bg-[#2F363D] tex-white`

</script>
<template>
    <div :class="classLayoutHeader">
        <headerComponent/>
        <breadCrumbComponent/>
    </div>
</template>
