<script setup>
import FollowingItem from "@/Components/app/FollowingItem.vue";
import TextInput from "@/Components/TextInput.vue";
import {ref} from 'vue';
const searchKeyword = ref('')
</script>
<template>
    <div class="bg-white rounded mt-6 border p-3 sticky top-6">
        <div class="text-2xl font-bold pb-6 pt-3">My Friend</div>
             <TextInput :model="searchKeyword" placeholder="Type to search" class="w-full"/>
            <div class="mt-4">
                <div v-if="false" class="text-gray-500 p-3">
                    You don't have friends yet
                </div>
                <div v-else class="overflow-scroll h-[220px] lg:h-[450px]">
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title="John Doe"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title=" Elon Musk"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title="John Doe"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title=" Elon Musk"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title="John Doe"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title=" Elon Musk"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title="John Doe"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title=" Elon Musk"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title="John Doe"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title=" Elon Musk"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title="John Doe"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title=" Elon Musk"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title="John Doe"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title=" Elon Musk"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title="John Doe"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title=" Elon Musk"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title="John Doe"
                    />
                    <FollowingItem
                        image="https://picsum.photos/50"
                        title=" Elon Musk"
                    />
                </div>
            </div>
    </div>
</template>

