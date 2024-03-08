<script setup>
import { Head, Link } from "@inertiajs/vue3";
import GroupList from "@/Components/app/GroupList.vue";
import FollowingList from "@/Components/app/FollowingList.vue";
import PostList from "@/Components/app/PostList.vue";
import CreatePost from "@/Components/app/CreatePost.vue"
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";


defineProps({});
</script>

<template>
    <Head title="Social Media Website" />
    <AuthenticatedLayout>
        <div class="grid lg:grid-cols-12">
            <div class="lg:col-span-3 px-3  lg:order-1 ">
                <GroupList/>
            </div>
            <div class="lg:col-span-3 px-3 lg:order-3">
                <FollowingList/>
            </div>
            <div class="lg:col-span-6 lg:order-2">
                <CreatePost/>
                <PostList/>
            </div>
        </div>
    </AuthenticatedLayout>
</template>
