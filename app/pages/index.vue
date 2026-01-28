<script setup lang="ts">
definePageMeta({
  layout: 'front'
})

const router = useRouter()
</script>

<template>
  <div class="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100 dark:from-gray-900 dark:to-gray-800 flex items-center justify-center">
    <div class="text-center max-w-4xl mx-auto p-8">
      <!-- Logo -->
      <div class="mb-8">
        <h1 class="text-5xl font-bold text-blue-600 dark:text-blue-400 mb-2">
          Nuxt Dashboard
        </h1>
        <p class="text-xl text-gray-600 dark:text-gray-300">
          A modern admin dashboard built with Nuxt 4, Shadcn Vue, and TailwindCSS
        </p>
      </div>

      <!-- Main Content -->
      <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-xl p-8 mb-8">
        <h2 class="text-2xl font-semibold text-gray-900 dark:text-white mb-4">
          Welcome to our Dashboard
        </h2>
        <p class="text-gray-600 dark:text-gray-300 mb-6">
          This is the public front page of our application. Access the admin dashboard to manage your account, view analytics, and more.
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <button 
            @click="router.push('/admin')"
            class="px-6 py-3 bg-blue-600 hover:bg-blue-700 text-white font-medium rounded-lg transition-colors"
          >
            Access Admin Dashboard
          </button>
          <button 
            @click="router.push('/login')"
            class="px-6 py-3 bg-gray-200 hover:bg-gray-300 dark:bg-gray-700 dark:hover:bg-gray-600 text-gray-800 dark:text-white font-medium rounded-lg transition-colors"
          >
            Login
          </button>
        </div>
      </div>

      <!-- Features -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
        <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg p-6">
          <div class="text-blue-500 dark:text-blue-400 text-3xl mb-4">
            📊
          </div>
          <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-2">
            Analytics
          </h3>
          <p class="text-gray-600 dark:text-gray-300">
            Track your website's performance with detailed analytics
          </p>
        </div>
        <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg p-6">
          <div class="text-green-500 dark:text-green-400 text-3xl mb-4">
            ✅
          </div>
          <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-2">
            Task Management
          </h3>
          <p class="text-gray-600 dark:text-gray-300">
            Organize and prioritize your tasks efficiently
          </p>
        </div>
        <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg p-6">
          <div class="text-purple-500 dark:text-purple-400 text-3xl mb-4">
            🎨
          </div>
          <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-2">
            Customizable
          </h3>
          <p class="text-gray-600 dark:text-gray-300">
            Personalize your dashboard with themes and layouts
          </p>
        </div>
      </div>

      <!-- Footer -->
      <footer class="text-gray-500 dark:text-gray-400 text-sm">
        <p>© {{ new Date().getFullYear() }} Nuxt Dashboard. All rights reserved.</p>
      </footer>
    </div>
  </div>
</template>