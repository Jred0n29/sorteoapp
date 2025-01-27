<script>
export default {
  data() {
    return {
      menuItems: [
        { text: 'Inicio', href: '#Inicio' },
        { text: 'Preguntas F', href: '#Preguntas' },
        { text: 'Testimonios', href: '#Testimonios' },
        { text: 'Contacto', href: '#Contacto' }
      ],
      isMenuOpen: false, // Estado para controlar la visibilidad del menú
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    }
  }
};
</script>

<template>
  <nav class="bg-emerald-100 border-b-[1px] border-black-medium dark:border-none dark:bg-neutral-800">
    <div class="gap-y-2 flex flex-col md:max-w-screen-xl md:flex-row flex-wrap items-center justify-between mx-auto p-4">
      <a href="" class="flex items-center space-x-3 rtl:space-x-reverse">
        <img src="/src/assets/clover.svg" class="h-12" alt="Logo trebol">
        <span class="self-center text-primary-black text-2xl font-bold whitespace-nowrap">El Trebol</span>
      </a>
      <div class="flex flex-col md:flex-row items-center md:order-2 space-x-1 md:space-x-0 rtl:space-x-reverse">
        <button
          type="button"
          class="text-primary-green border-2 border-primary-green flex flex-row gap-x-2 items-center font-bold rounded-lg text-sm px-5 py-2.5 text-center"
        >
          Unete a Wpp!
          <img src="/src/assets/wppcolor.svg" class="h-8" alt="Logo">
        </button>

        <!-- Botón de despliegue del menú -->
        <button
          id="theme-toggletwo"
          type="button"
          class="inline-flex items-center w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
          @click="toggleMenu"
          :aria-expanded="isMenuOpen"
        >
          <span class="sr-only">Open main menu</span>
          <svg class="w-5 h-5" aria-hidden="true" fill="none" viewBox="0 0 17 14">
            <path
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M1 1h15M1 7h15M1 13h15"
            ></path>
          </svg>
        </button>
      </div>

      <!-- Menú desplegable -->
      <div
        class="items-center justify-between w-full md:flex md:w-auto md:order-1"
        id="navbar-language"
        :class="{ hidden: !isMenuOpen }"
      >
        <ul class="flex flex-col font-medium p-4 md:p-0 mt-4 border border-gray-100 md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0 items-center">
          <li v-for="item in menuItems" :key="item.href">
            <a :href="item.href" class="block py-2 px-3 text-primary-black md:p-0">
              {{ item.text }}
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
