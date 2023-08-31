<script setup>
import axios from "axios";
import {ref} from "vue";

const postDetails = ref('')

post();
async function post() {
    let url = "https://basic-blog.teamrabbil.com/api/post-details/53"
    let res = await axios.get(url)
    postDetails.value = res.data.postDetails
    console.log(res.data.postDetails)
}
</script>

<template>
  <div class="mx-auto max-w-7xl mt-10 mb-10">
    <div class="border rounded">
      <div class="relative">
        <img :src="postDetails.img" alt="" />

<!--        <h2-->
<!--          class="text-4xl font-bold p-5 text-white text-center absolute bottom-40 left-10 bg-green-950 w-1/3"-->
<!--        >-->
<!--            {{ postDetails.title.slice(0,20) }}-->
<!--        </h2>-->
<!--        <h3-->
<!--          class="text-4xl font-bold p-5 text-white text-center absolute bottom-16 left-10 bg-orange-950 w-1/3"-->
<!--        >-->
<!--            {{ postDetails.title.slice(21) }}-->
<!--        </h3>-->
      </div>

      <div class="p-10">
        <div class="">
          <h2 class="font-bold text-xl mb-10">
              {{ postDetails.title }}
          </h2>
          <p>
              {{ postDetails.content }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
