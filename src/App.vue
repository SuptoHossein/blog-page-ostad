<script setup>
import {RouterLink, RouterView} from 'vue-router'
import axios from "axios";
import {ref} from "vue";

const categoryData = ref('');

categories();

async function categories() {
  let url = "https://basic-blog.teamrabbil.com/api/post-categories"
  let res = await axios.get(url)
  categoryData.value = res.data
}
</script>

<template>
  <nav class="bg-white">
    <div class="mx-auto max-full px-2 sm:px-6 lg:px-8 border-t-2 border-b-2 border-gray-200">
      <div class="relative flex h-16 items-center justify-between">
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
          <!-- Mobile menu button-->
          <button
              type="button"
              class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
              aria-controls="mobile-menu"
              aria-expanded="false"
          >
            <span class="absolute -inset-0.5"></span>
            <span class="sr-only">Open main menu</span>
            <svg
                class="block h-6 w-6"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                aria-hidden="true"
            >
              <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
              />
            </svg>
            <svg
                class="hidden h-6 w-6"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                aria-hidden="true"
            >
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/>
            </svg>
          </button>
        </div>

        <!--          menu -->
        <div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">
          <div class="flex flex-shrink-0 items-center">
            <h3 class="font-bold">
                <RouterLink to="/">MR BLOG</RouterLink>
            </h3>
          </div>
        </div>
        <div
            class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0"
        >
          <!-- Profile dropdown -->
          <div class="relative ml-3">
            <div class="hidden sm:ml-6 sm:block">
              <div class="flex space-x-4">
                <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->


                <RouterLink class="bg-gray-300 hover:bg-gray-200 text-gray-900 rounded-md px-3 py-2 text-sm font-medium"
                            to="/"
                >হোম
                </RouterLink>
                <RouterLink v-for="category in categoryData" :key="category.id"
                            class="bg-gray-300 text-gray-900 hover:bg-gray-200 rounded-md px-3 py-2 text-sm font-medium"
                            to="/"
                >{{ category.name }}
                </RouterLink>

              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="sm:hidden" id="mobile-menu">
      <div class="space-y-1 px-2 pb-3 pt-2">
        <RouterLink class="bg-gray-900 text-white rounded-md px-3 py-2 text-sm font-medium" to="/"
        >Home
        </RouterLink>
      </div>
    </div>
  </nav>


  <!--    Router View   -->
  <RouterView/>


    <div class="bg-gray-100 mt-10">
        <div class="mx-auto max-w-7xl py-2">
            <p class="text-gray-600">Copyright &copy; {{ new Date().getFullYear() }}</p>
        </div>
    </div>

</template>
