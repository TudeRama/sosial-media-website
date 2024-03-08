<script setup>
import {ref} from "vue";
const postCreating = ref(false)
</script>
<template>
    <div class="pt-6 pb-3 bg-white px-4 my-6 rounded border sticky top-0 lg:top-6 z-50">
        <div @click="postCreating = true" class="text-gray-500 border py-3 px-2 mb-3 rounded">Click here to create new post</div>
        <div v-if="postCreating" class="flex justify-between">
            <button
                type="submit"
                class="rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600 relative"
            >
                Attach File
                <input type="file" class="absolute top-0 left-0 bottom-0 right-0 opacity-0">
            </button>
            <button
                type="submit"
                class="rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
            >
                Submit
            </button>
        </div>
    </div>
</template>
