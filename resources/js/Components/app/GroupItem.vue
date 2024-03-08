<script setup>
defineProps({
    image: String,
    title: String,
    description: String,
});
</script>
<template>
    <div class="flex items-center gap-3 hover:bg-gray-100 px-6 py-3">
        <img :src="image" alt="" class="w-12 h-12 rounded-full" />
        <div>
            <div class="font-bold text-lg">{{ title }}</div>
            <div class="text-xs text-gray-500">{{ description }}</div>
        </div>
    </div>
</template>
