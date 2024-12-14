<template>
    <div class="flex">
        <SideBar />
        <div class="flex-1 flex flex-col">
            <Notifications />
            <HomeContent />
        </div>
    </div>
</template>

<script setup>
import SideBar from '../components/SideBar.vue';
import Notifications from '@/components/Notifications.vue';
import HomeContent from '@/components/HomeContent.vue';
</script>
