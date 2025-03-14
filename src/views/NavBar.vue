<template>
  <nav class="bg-white dark:bg-gray-900 shadow-md">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16 items-center">

        <div class="flex-shrink-0">
          <img src="https://via.placeholder.com/50" alt="Logo" class="h-10 w-10">
        </div>

        <!-- Navigation Links -->
        <div class="hidden md:flex space-x-6">
          <a href="#" class="text-gray-700 dark:text-gray-300 hover:text-blue-500">Home</a>
          <a href="#" class="text-gray-700 dark:text-gray-300 hover:text-blue-500">About</a>
          <a href="#" class="text-gray-700 dark:text-gray-300 hover:text-blue-500">Services</a>
          <a href="#" class="text-gray-700 dark:text-gray-300 hover:text-blue-500">Contact</a>
        </div>

        <!-- Mobile Menu Button -->
        <div class="md:hidden">
          <button @click="toggleMenu" class="text-gray-700 dark:text-gray-300 focus:outline-none">
            ☰
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Dropdown Menu -->
    <div v-if="isOpen" class="md:hidden bg-white dark:bg-gray-900">
      <a href="#"
         class="block px-4 py-2 text-gray-700 dark:text-gray-300 hover:bg-gray-200 dark:hover:bg-gray-700">Home</a>
      <a href="#" class="block px-4 py-2 text-gray-700 dark:text-gray-300 hover:bg-gray-200 dark:hover:bg-gray-700">About</a>
      <a href="#" class="block px-4 py-2 text-gray-700 dark:text-gray-300 hover:bg-gray-200 dark:hover:bg-gray-700">Services</a>
      <a href="#" class="block px-4 py-2 text-gray-700 dark:text-gray-300 hover:bg-gray-200 dark:hover:bg-gray-700">Contact</a>
    </div>
  </nav>
</template>
<script>
export default {
  name: 'NavBar'
}
</script>