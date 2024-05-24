<script setup lang="ts">
import { ref } from 'vue'
import IconLogo from '@/components/icons/IconLogo.vue'
import { RouterLink } from 'vue-router'

const activeMenu = ref(false)

function closeMenu() {
  activeMenu.value = false
}
</script>
<template>
  <header class="flex items-center justify-between px-4 gap-8 border-b-2 border-b-indigo-100 h-20">
    <RouterLink to="/" @click="closeMenu">
      <IconLogo />
    </RouterLink>
    <button
      class="relative z-10 flex h-3 w-6 flex-col justify-between lg:hidden *:block *:ease *:h-[2px] *:w-full *:transform *:rounded-full *:bg-black *:transition *:duration-300"
      @click="activeMenu = !activeMenu"
    >
      <span :class="{ 'translate-y-[5px] rotate-45': activeMenu }"></span>
      <span :class="{ '-translate-y-[5px] -rotate-45': activeMenu }"></span>
    </button>
    <nav
      class="invisible opacity-0 flex-1 px-6 py-12 flex justify-between mt-20 flex-col fixed z-10 inset-0 bg-indigo-50 lg:mt-0 lg:flex-row lg:static lg:bg-transparent lg:py-6 lg:visible lg:opacity-100"
      :class="{ '!visible !opacity-100': activeMenu }"
      v-scroll-lock="activeMenu"
    >
      <ul class="flex flex-col gap-4 lg:flex-row">
        <li>
          <RouterLink
            class="block p-4 rounded-lg text-gray-500"
            to="/properties/"
            @click="closeMenu"
            >Rent</RouterLink
          >
        </li>
        <li>
          <RouterLink class="block p-4 rounded-lg text-gray-500" to="/buy" @click="closeMenu"
            >Buy</RouterLink
          >
        </li>
        <li>
          <RouterLink class="block p-4 rounded-lg text-gray-500" to="/sell" @click="closeMenu"
            >Sell</RouterLink
          >
        </li>
        <li>
          <RouterLink class="block p-4 rounded-lg text-gray-500" to="/manage" @click="closeMenu"
            >Manage property</RouterLink
          >
        </li>
        <li>
          <RouterLink class="block p-4 rounded-lg text-gray-500" to="/resources" @click="closeMenu"
            >Resources</RouterLink
          >
        </li>
      </ul>
      <div class="flex items-center justify-center gap-4 px-4">
        <a
          class="flex-1 text-center px-6 py-3 text-base text-indigo-500 border-2 font-bold rounded-lg transition duration-300 ease-in-out"
          href="/"
          >Login</a
        >
        <a
          class="flex-1 text-center px-6 py-3 text-base text-indigo-500 border-2 font-bold rounded-lg transition duration-300 ease-in-out border border-indigo-500 bg-indigo-500 text-white"
          href="/"
          >Signup</a
        >
      </div>
    </nav>
  </header>
</template>
