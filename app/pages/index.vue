<script setup lang="ts">
definePageMeta({
  layout: 'front'
})

import { ref } from 'vue'

const mobileMenuOpen = ref(false)
</script>

<template>
  <div class="min-h-screen flex flex-col">
    <!-- Header/Navigation -->
    <header class="bg-white dark:bg-gray-900 shadow-sm sticky top-0 z-50">
      <div class="@container/main px-4 py-4">
        <div class="flex items-center justify-between">
          <div class="flex items-center">
            <h1 class="text-sm md:text-xl font-semibold text-gray-900 dark:text-white">
              清华大学膜生物学国家重点实验室
            </h1>
          </div>
          
          <!-- Mobile Menu Button -->
          <button 
            class="md:hidden text-gray-700 dark:text-gray-300"
            @click="mobileMenuOpen = !mobileMenuOpen"
          >
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>
          </button>
          
          <!-- Desktop Navigation -->
          <nav class="hidden md:flex items-center space-x-6">
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors">
              实验室概况
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors">
              科研团队
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors">
              科研平台
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors">
              新闻中心
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors">
              党群文化
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors">
              人才招聘
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors">
              联系我们
            </a>
          </nav>
        </div>
        
        <!-- Mobile Navigation -->
        <div v-if="mobileMenuOpen" class="md:hidden mt-4 pb-4 border-t border-gray-200 dark:border-gray-700">
          <nav class="flex flex-col space-y-3">
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors py-2">
              实验室概况
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors py-2">
              科研团队
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors py-2">
              科研平台
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors py-2">
              新闻中心
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors py-2">
              党群文化
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors py-2">
              人才招聘
            </a>
            <a href="#" class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white transition-colors py-2">
              联系我们
            </a>
          </nav>
        </div>
      </div>
    </header>

    <!-- Main Banner -->
    <main class="flex-1">
      <div class="relative w-full h-[400px] md:h-[600px]">
        <img 
          src="https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=Interior%20of%20a%20modern%20conference%20hall%20with%20a%20large%20purple%20stage%20backdrop%20featuring%20Chinese%20text%20about%20Tsinghua%20University%20laboratory%20opening%20ceremony%2C%20professional%20lighting%2C%20wooden%20walls%2C%20academic%20atmosphere&image_size=landscape_16_9" 
          alt="实验室揭牌仪式" 
          class="w-full h-full object-cover"
        />
        <div class="absolute inset-0 flex items-center justify-center bg-black bg-opacity-30">
          <div class="text-center text-white px-4">
            <h2 class="text-lg md:text-2xl lg:text-3xl font-bold mb-2">
              清华大学膜生物学国家重点实验室
            </h2>
            <h3 class="text-xl md:text-3xl lg:text-4xl font-bold mb-3 md:mb-4">
              膜结构及人工智能生物学分室
            </h3>
            <p class="text-sm md:text-lg mb-2">
              暨清华大学-北京大学生命科学联合中心
            </p>
            <p class="text-sm md:text-lg">
              2024年暑期学校启动仪式
            </p>
          </div>
        </div>
      </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-400 py-6 md:py-8">
      <div class="@container/main px-4">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
          <div>
            <h4 class="text-base md:text-lg font-semibold text-white mb-3 md:mb-4">
              清华大学膜生物学国家重点实验室
            </h4>
            <p class="text-xs md:text-sm mb-2">
              膜结构及人工智能生物学分室
            </p>
            <p class="text-xs md:text-sm">
              清华大学生命科学院
            </p>
          </div>
          <div class="text-xs md:text-sm">
            <p class="mb-1">
              <span class="text-gray-300">公司：</span> 膜生物学国家重点实验室膜结构及人工智能生物学分室
            </p>
            <p class="mb-1">
              <span class="text-gray-300">电话：</span> 0571-61109099
            </p>
            <p class="mb-1">
              <span class="text-gray-300">邮箱：</span> thu-msi@othu-msa.org.cn
            </p>
            <p>
              <span class="text-gray-300">地址：</span> 浙江省杭州市临安区青山湖街道大园路1623号强国分量室
            </p>
          </div>
        </div>
        <div class="border-t border-gray-700 mt-4 md:mt-6 pt-4 md:pt-6 text-xs text-center">
          <p class="leading-relaxed">
            Copyright © 2025 膜生物学国家重点实验室膜结构及人工智能生物学分室 版权所有 | ICP备2025166305号-1
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>