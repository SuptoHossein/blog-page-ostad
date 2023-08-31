<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <nav class="bg-white">
    <div class="mx-auto max-full px-2 sm:px-6 lg:px-8 border-t-2 border-b-2 border-gray-300">
      <div class="relative flex h-16 items-center justify-between">
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
          <!-- Mobile menu button-->
          <button type="button"
            class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
            aria-controls="mobile-menu" aria-expanded="false">
            <span class="absolute -inset-0.5"></span>
            <span class="sr-only">Open main menu</span>
            <svg class="block h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
              aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>
            <svg class="hidden h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
              aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
        <div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">
          <div class="flex flex-shrink-0 items-center">
            <h3 class="font-bold">MR BLOG</h3>
          </div>
        </div>
        <div class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0">


          <!-- Profile dropdown -->
          <div class="relative ml-3">

            <div class="hidden sm:ml-6 sm:block">
              <div class="flex space-x-4">
                <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
                <RouterLink class="bg-gray-300 text-gray-900 rounded-md px-3 py-2 text-sm font-medium" to="/">হোম
                </RouterLink>
                <RouterLink
                  class="text-gray-900 hover:bg-gray-300 hover:text-gray-900 rounded-md px-3 py-2 text-sm font-medium"
                  to="/">ইতিহাস</RouterLink>
                <RouterLink
                  class="text-gray-900 hover:bg-gray-300 hover:text-gray-900 rounded-md px-3 py-2 text-sm font-medium"
                  to="/">লাইব্রেরী</RouterLink>
                <RouterLink
                  class="text-gray-900 hover:bg-gray-300 hover:text-gray-900 rounded-md px-3 py-2 text-sm font-medium"
                  to="/">খেলাধুলা</RouterLink>
                <RouterLink
                  class="text-gray-900 hover:bg-gray-300 hover:text-gray-900 rounded-md px-3 py-2 text-sm font-medium"
                  to="/">বাংলাদেশ</RouterLink>
                <RouterLink
                  class="text-gray-900 hover:bg-gray-300 hover:text-gray-900 rounded-md px-3 py-2 text-sm font-medium"
                  to="/">বিশ্ব</RouterLink>
                <RouterLink
                  class="text-gray-900 hover:bg-gray-300 hover:text-gray-900 rounded-md px-3 py-2 text-sm font-medium"
                  to="/">বই ও ছিনেমা</RouterLink>
                <RouterLink
                  class="text-gray-900 hover:bg-gray-300 hover:text-gray-900 rounded-md px-3 py-2 text-sm font-medium"
                  to="/">বিজ্ঞান</RouterLink>
                <RouterLink
                  class="text-gray-900 hover:bg-gray-300 hover:text-gray-900 rounded-md px-3 py-2 text-sm font-medium"
                  to="/">বিজ্ঞানী</RouterLink>
                <RouterLink
                  class="text-gray-900 hover:bg-gray-300 hover:text-gray-900 rounded-md px-3 py-2 text-sm font-medium"
                  to="/">উপকথা</RouterLink>

              </div>
            </div>


          </div>
        </div>
      </div>
    </div>

    <!-- Mobile menu, show/hide based on menu state. -->
    <div class="sm:hidden" id="mobile-menu">
      <div class="space-y-1 px-2 pb-3 pt-2">
        <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
        <RouterLink class="bg-gray-900 text-white rounded-md px-3 py-2 text-sm font-medium" to="/">হোম</RouterLink>
        <RouterLink class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
          to="/">ইতিহাস</RouterLink>
        <RouterLink class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
          to="/">লাইব্রেরী</RouterLink>
        <RouterLink class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
          to="/">খেলাধুলা</RouterLink>
        <RouterLink class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
          to="/">বাংলাদেশ</RouterLink>
        <RouterLink class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
          to="/">বিশ্ব</RouterLink>
        <RouterLink class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
          to="/">বই ও ছিনেমা</RouterLink>
        <RouterLink class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
          to="/">বিজ্ঞান</RouterLink>
        <RouterLink class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
          to="/">বিজ্ঞানী</RouterLink>
        <RouterLink class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
          to="/">উপকথা</RouterLink>

      </div>
    </div>
  </nav>


  <div class="mx-auto max-w-7xl mt-10 mb-10">
    <div class="border rounded-t">
      <div class="relative">
        <img
          src="https://images.unsplash.com/photo-1692902295604-6c5109aa55a4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1632&q=80"
          alt="">
      </div>
      <div class="">
        <h2 class="text-4xl font-bold p-5 text-white text-center absulate bottom-10 left-10 bg-green-900 mb-2 w-1/3">তামিমের বিকল্প ভাবার</h2>
        <h3 class="text-4xl font-bold p-5 text-white text-center absulate bottom-10 left-10 bg-green-900 mb-2 w-1/3">সময়তো নেই!</h3>
      </div>
    </div>

    <div class="p-10">
      <div class="">
        <h2 class="font-bold text-xl mb-10">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Numquam, sit.</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti quos illum sequi reiciendis ipsa pariatur,
          laudantium officiis? Qui, sunt consequuntur iste magni, saepe accusamus cumque tempora labore quos nihil
          provident expedita vel atque corrupti quae voluptatibus eius, explicabo velit aspernatur dicta sint inventore
          deserunt voluptatum quasi? Quas nostrum autem est atque necessitatibus, praesentium enim totam iure,
          exercitationem esse inventore. Impedit mollitia labore, aliquid explicabo pariatur id eligendi ratione sed
          deserunt libero aperiam quam perspiciatis culpa quia vitae saepe vel qui a non! Dolore saepe, assumenda pariatur
          odit cumque provident! Nostrum eum maxime alias, nulla vel quos molestias ipsa blanditiis rerum, libero ipsum
          nesciunt delectus! Molestiae ipsum id veniam ipsa nemo excepturi ducimus dicta quod quibusdam explicabo autem
          quo veritatis laborum aspernatur necessitatibus dolorem dolorum, molestias tenetur. Deleniti nostrum suscipit
          maxime accusantium impedit atque autem aperiam aliquam? Obcaecati veritatis facere sed, enim eius soluta dolore
          totam corporis voluptates similique rerum blanditiis doloribus quidem id ex repellat assumenda, sunt accusamus
          quae unde vel sit a illo nihil. Iusto, dignissimos veniam id consequatur aliquam iure pariatur accusantium
        voluptatem eligendi nostrum, error dolore eaque possimus voluptate rerum numquam expedita similique mollitia
        totam quo temporibus distinctio, eum placeat. Laborum itaque dolorem animi pariatur nihil est magni explicabo
        porro rerum dolorum assumenda fugit officiis, tempora voluptas earum quia? Soluta sint, commodi exercitationem
        quam officiis beatae natus magnam magni blanditiis officia quas laborum voluptatum cumque alias velit
        repudiandae architecto delectus eos animi eligendi adipisci. Architecto rerum, labore dolores temporibus laborum
        pariatur quam excepturi, sed ut corporis officia praesentium! Quo, eaque cupiditate? Commodi aut id illum
        recusandae tempora deleniti in dolorum consequatur sapiente? Quos nulla illo aut mollitia ullam, nostrum sed ea
        fugiat dolores velit, assumenda incidunt, maiores eum obcaecati provident! Provident impedit eligendi officiis
        nam nobis praesentium vel accusamus. Quibusdam praesentium culpa voluptatem ut sequi laboriosam et!</p>
    </div>
  </div>
</div>



<RouterView /></template>


