<template>
    <AuthenticatedLayout>
        <div class="lg:mx-20">
            <div class="relative bg-white">
                <img
                    src="https://timelinecovers.pro/facebook-cover/download/ultra-hd-space-facebook-cover.jpg"
                    alt=""
                    class="w-full h-60 object-cover"
                />
                <div class="flex">
                    <img
                        src="https://randomuser.me/api/portraits/men/44.jpg"
                        alt=""
                        class="ml-16 -mt-14 rounded-full"
                    />
                    <div class="flex justify-between items-center px-4 w-full">
                        <div class="text-xl font-bold">
                            {{ user.name }}
                        </div>
                        <PrimaryButton v-if="authUser && authUser.id == user.id">
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                fill="none"
                                viewBox="0 0 24 24"
                                stroke-width="1.5"
                                stroke="currentColor"
                                class="w-4 h-4 mr-2"
                            >
                                <path
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                    d="m16.862 4.487 1.687-1.688a1.875 1.875 0 1 1 2.652 2.652L6.832 19.82a4.5 4.5 0 0 1-1.897 1.13l-2.685.8.8-2.685a4.5 4.5 0 0 1 1.13-1.897L16.863 4.487Zm0 0L19.5 7.125"
                                />
                            </svg>

                            Edit Profile
                        </PrimaryButton>
                    </div>
                </div>
            </div>
            <div class="border-t">
                <TabGroup>
                    <TabList class="flex bg-white">
                        <Tab v-if="authUser && authUser.id == user.id" as="template" key="post" v-slot="{ selected }">
                            <button
                                :class="[
                                    'px-4 py-2.5 outline-none',
                                    selected
                                        ? 'bg-blue-50 text-blue-800 border-b-2 border-blue-500'
                                        : 'text-gray-900',
                                ]"
                            >
                                About
                            </button>
                        </Tab>
                        <Tab as="template" key="post" v-slot="{ selected }">
                            <button
                                :class="[
                                    'px-4 py-2.5 outline-none',
                                    selected
                                        ? 'bg-blue-50 text-blue-800 border-b-2 border-blue-500'
                                        : 'text-gray-900',
                                ]"
                            >
                                Post
                            </button>
                        </Tab>
                        <Tab as="template" key="post" v-slot="{ selected }">
                            <button
                                :class="[
                                    'px-4 py-2.5 outline-none',
                                    selected
                                        ? 'bg-blue-50 text-blue-800 border-b-2 border-blue-500'
                                        : 'text-gray-900',
                                ]"
                            >
                                Followers
                            </button>
                        </Tab>
                        <Tab as="template" key="post" v-slot="{ selected }">
                            <button
                                :class="[
                                    'px-4 py-2.5 outline-none',
                                    selected
                                        ? 'bg-blue-50 text-blue-800 border-b-2 border-blue-500'
                                        : 'text-gray-900',
                                ]"
                            >
                                Following
                            </button>
                        </Tab>
                        <Tab as="template" key="post" v-slot="{ selected }">
                            <button
                                :class="[
                                    'px-4 py-2.5 outline-none',
                                    selected
                                        ? 'bg-blue-50 text-blue-800 border-b-2 border-blue-500'
                                        : 'text-gray-900',
                                ]"
                            >
                                Photos
                            </button>
                        </Tab>
                    </TabList>

                    <TabPanels class="mt-2">
                        <TabPanel v-if="authUser && authUser.id == user.id">
                            <Edit
                                :must-verify-email="mustVerifyEmail"
                                :status="status"
                            />
                        </TabPanel>
                        <TabPanel class="bg-white p-3 shadow">
                            Post Content
                        </TabPanel>
                        <TabPanel class="bg-white p-3 shadow">
                            Followers Content
                        </TabPanel>
                        <TabPanel class="bg-white p-3 shadow">
                            Following Content
                        </TabPanel>
                        <TabPanel class="bg-white p-3 shadow">
                            Photos Content
                        </TabPanel>
                    </TabPanels>
                </TabGroup>
            </div>
        </div>
    </AuthenticatedLayout>
</template>

<script setup>
import { ref } from "vue";
import { TabGroup, TabList, Tab, TabPanels, TabPanel } from "@headlessui/vue";
import { usePage } from "@inertiajs/vue3";
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import Edit from "@/Pages/Profile/Edit.vue";
import PrimaryButton from "@/Components/PrimaryButton.vue";
const authUser = usePage().props.auth.user;
defineProps({
    mustVerifyEmail: {
        type: Boolean,
    },
    status: {
        type: String,
    },
    user:{
        type: Object
    }
});


const categories = ref({
    Recent: [
        {
            id: 1,
            title: "Does drinking coffee make you smarter?",
            date: "5h ago",
            commentCount: 5,
            shareCount: 2,
        },
        {
            id: 2,
            title: "So you've bought coffee... now what?",
            date: "2h ago",
            commentCount: 3,
            shareCount: 2,
        },
    ],
    Popular: [
        {
            id: 1,
            title: "Is tech making coffee better or worse?",
            date: "Jan 7",
            commentCount: 29,
            shareCount: 16,
        },
        {
            id: 2,
            title: "The most innovative things happening in coffee",
            date: "Mar 19",
            commentCount: 24,
            shareCount: 12,
        },
    ],
    Trending: [
        {
            id: 1,
            title: "Ask Me Anything: 10 answers to your questions about coffee",
            date: "2d ago",
            commentCount: 9,
            shareCount: 5,
        },
        {
            id: 2,
            title: "The worst advice we've ever heard about coffee",
            date: "4d ago",
            commentCount: 1,
            shareCount: 2,
        },
    ],
});
</script>
