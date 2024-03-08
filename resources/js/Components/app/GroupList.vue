<script setup>
import GroupItem from "@/Components/app/GroupItem.vue";
import TextInput from "@/Components/TextInput.vue";
import {ref} from 'vue';
const searchKeyword = ref('')
</script>
<template>
    <div class="bg-white rounded mt-6 border p-3 sticky top-6">
        <div class="text-2xl font-bold pt-3 pb-6">My Group</div>
             <TextInput :model="searchKeyword" placeholder="Type to search" class="w-full"/>
            <div class="mt-4">
                <div v-if="false" class="text-gray-500 p-3">
                    You are not joined to any group
                </div>
                <div v-else class="overflow-scroll h-[220px] lg:h-[450px]">
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Laravel Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Vue Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Laravel Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Vue Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Laravel Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Vue Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Laravel Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Vue Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Laravel Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Vue Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Laravel Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Vue Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Laravel Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Vue Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Laravel Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                    <GroupItem
                        image="https://picsum.photos/50"
                        title="Vue Developer"
                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, eum!"
                    />
                </div>
            </div>
    </div>
</template>

