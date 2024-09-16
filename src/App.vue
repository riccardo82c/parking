<template>
  <div class="min-h-screen bg-gray-100 flex flex-col">

    <nav class="bg-white shadow-lg">
      <div class="max-w-6xl mx-auto px-4">
        <div class="flex justify-between">
          <div class="flex space-x-7">
            <div>
              <a href="#" class="flex items-center py-4 px-2">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="100" height="100">
                  <!-- Cerchio principale -->
                  <circle cx="50" cy="50" r="45" fill="none" stroke="black" stroke-width="5" />

                  <!-- P stilizzata -->
                  <path d="M40 65 V35 A10 10 0 0 1 50 25 H60 A10 10 0 0 1 60 45 H50 V65 Z" fill="black" />
                </svg>


                <!-- <span class="font-semibold text-gray-500 text-lg">Logo</span> -->
              </a>
            </div>
            <div class="hidden md:flex items-center space-x-1">
              <router-link to="/"
                class="py-4 px-2 text-gray-500 font-semibold hover:text-cyan-500 transition duration-300">Home</router-link>
              <router-link to="/chi-siamo"
                class="py-4 px-2 text-gray-500 font-semibold hover:text-cyan-500 transition duration-300">Chi
                Siamo</router-link>
              <router-link to="/servizi"
                class="py-4 px-2 text-gray-500 font-semibold hover:text-cyan-500 transition duration-300">Servizi</router-link>
              <router-link to="/contatti"
                class="py-4 px-2 text-gray-500 font-semibold hover:text-cyan-500 transition duration-300">Contatti</router-link>
            </div>
          </div>
          <!-- Menu Hamburger per mobile -->
          <div class="md:hidden flex items-center">
            <button @click="toggleMobileMenu" class="outline-none mobile-menu-button">
              <svg class="w-6 h-6 text-gray-500 hover:text-cyan-500" x-show="!showMenu" fill="none"
                stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24"
                stroke="currentColor">
                <path d="M4 6h16M4 12h16M4 18h16"></path>
              </svg>
            </button>
          </div>
        </div>
      </div>
      <!-- Menu mobile -->
      <div class="md:hidden" v-show="showMobileMenu">
        <router-link to="/" class="block py-2 px-4 text-sm hover:bg-gray-200">Home</router-link>
        <router-link to="/chi-siamo" class="block py-2 px-4 text-sm hover:bg-gray-200">Chi Siamo</router-link>
        <router-link to="/servizi" class="block py-2 px-4 text-sm hover:bg-gray-200">Servizi</router-link>
        <router-link to="/contatti" class="block py-2 px-4 text-sm hover:bg-gray-200">Contatti</router-link>
      </div>
    </nav>

    <div class="flex-grow flex items-center justify-center p-4">
      <div class="w-full max-w-4xl mx-auto">
        <div class="relative py-3">
          <div
            class="absolute inset-0 bg-gradient-to-r from-cyan-400 to-light-blue-500 shadow-lg transform -skew-y-6 sm:skew-y-0 sm:-rotate-6 sm:rounded-3xl">
          </div>
          <div class="relative bg-white shadow-lg sm:rounded-3xl px-4 py-10 sm:p-20">
            <router-view></router-view>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'App',
  setup() {
    const showMobileMenu = ref(false)

    const toggleMobileMenu = () => {
      showMobileMenu.value = !showMobileMenu.value
    }

    return {
      showMobileMenu,
      toggleMobileMenu
    }
  }
}
</script>
