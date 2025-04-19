<script setup>
import { ref } from 'vue';
const isMenuOpen = ref(false);
const Menu = ref([
  { name: 'Services', href: '#services' },
  { name: 'Projects', href: '#projects' },
  {name: 'Contact', href: '#contact'},
]);
const scrollToSection = (href) => {
  isMenuOpen.value = false;
  const section = document.querySelector(href);
  if (section) {
    section.scrollIntoView({
      behavior: 'smooth',
    });
  }
}
</script>

<template>
  <header class="max-w-full z-20">
    <nav class="flex border-b-2 border-b-primary2 items-center relative p-3 justify-between md:h-16 mx-auto
      md:px-4 container flex-wrap md:flex-nowrap"
    >
      <div class="text-3x1 font-bold flex text-primary">
        Logo
      </div>
      <div class="md:hidden z-30 ">
        <button class="block focus:outline-none" @click="isMenuOpen = !isMenuOpen">
          <span v-if="isMenuOpen" class="text-5x1">
            <img src="https://img.icons8.com/ios-filled/100/ffffff/delete-sign.png " alt="delete-sign"
            width="50" height="50"/>
          </span>
          <span v-else class="text-5x1">
            <img src="https://img.icons8.com/ios-filled/100/menu--v6.png " alt="delete-sign"
                 width="50" height="50"
            />
          </span>
        </button>
      </div>
        <!-- Resposive Menu -->
      <div :class="[
          'fixed inset-0 z-20 flex flex-col items-center justify-center bg-primary md:relative md:bg-transparent md:flex md:justify-between',
           isMenuOpen ? 'block' : 'hidden',
      ]">
        <ul class="flex flex-col items-center space-y-5 md:flex-row md:space-y-0 font-medium">
          <li v-for="item in Menu" :key="item.name">
            <a :href="item.href"
            class="block transition hover:text-primary ease-linear text-2x1 md:text-sm lg:text-lg text-white md:text-black"
            @click="scrollToSection(item.href)"
            >
              {{ item.name }}
            </a>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

