<script setup>
import {ref} from "vue";
import axios from "axios";

const blogList = ref('')

lists();
async function lists() {
    let url = "https://basic-blog.teamrabbil.com/api/post-list/1"
    let res= await axios.get(url)
    blogList.value = res.data
    console.log(res.data)
}
</script>

<template>
    <RouterLink to="/blog" class="mx-auto max-w-7xl lg:flex mt-10" v-for="blog in blogList" :key="blog.id">
<!--        <img :src="blog.img" alt="">-->
        <div class="h-48 lg:h-auto lg:w-48 flex-none bg-cover rounded-t lg:rounded-t-none lg:rounded-l text-center overflow-hidden" :style="{ 'background-image': 'url('+ blog.img +')' }" title="Woman holding a mug">
        </div>
        <div class="border-r border-b border-l border-gray-200 lg:border-l-0 lg:border-t lg:border-gray-200 bg-white rounded-b lg:rounded-b-none lg:rounded-r p-4 flex flex-col justify-between leading-normal">
            <div class="mb-8">
                <p class="text-sm text-gray-600 flex items-center">
                    <svg class="fill-current text-gray-500 w-3 h-3 mr-2" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
                        <path d="M4 8V6a6 6 0 1 1 12 0v2h1a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2v-8c0-1.1.9-2 2-2h1zm5 6.73V17h2v-2.27a2 2 0 1 0-2 0zM7 6v2h6V6a3 3 0 0 0-6 0z" />
                    </svg>
                    Members only
                </p>
                <div class="text-gray-900 font-bold text-xl mb-2">{{ blog.title }}</div>
                <p class="text-gray-700 text-base">{{ blog.short }}</p>
            </div>
            <div class="flex items-center">
                <div class="text-sm">
                    <p class="text-gray-900 leading-none">{{ blog.created_at }}</p>
                    <p class="text-gray-600">{{ blog.updated_at }}</p>
                </div>
            </div>
        </div>
    </RouterLink>

  <RouterView />
</template>
