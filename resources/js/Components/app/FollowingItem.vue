<script setup>
defineProps({
    image: String,
    title: String,
});
</script>
<template>
    <div class="flex items-center gap-3 hover:bg-gray-100 py-3 px-6">
        <img :src="image" alt="" class="w-12 h-12 rounded-full" />
        <div>
            <div class="font-bold">{{ title }}</div>
        </div>
    </div>
</template>
