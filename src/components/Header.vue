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
        <span class="self-center text-primary-black text-2xl font-bold whitespace-nowrap">The Clover</span>
      </a>
      <div class="flex flex-col md:flex-row items-center md:order-2 space-x-1 md:space-x-0 rtl:space-x-reverse">
        <a href="#_" class="box-border relative z-30 inline-flex items-center justify-center w-auto px-8 py-3 overflow-hidden font-bold text-white transition-all duration-500 bg-red-500 rounded-md cursor-pointer group ring-offset-2 ring-1 ring-red-300 ring-offset-red-200 ease focus:outline-none transform animate-pulseUpDown">
                    <span class="absolute bottom-0 right-0 w-8 h-20 -mb-8 -mr-5 transition-all duration-300 ease-out transform rotate-45 translate-x-1 bg-white opacity-20 group-hover:translate-x-0"></span>
                    <span class="absolute top-0 left-0 w-20 h-8 -mt-1 -ml-12 transition-all duration-300 ease-out transform -rotate-45 -translate-x-1 bg-white opacity-20 group-hover:translate-x-0"></span>
                    <span class="relative z-20 flex items-center text-sm">
                        Unete A Nuestro Grupo
                    </span>
                    <img class="w-6 h-6 me-2 ml-2" src="/src/assets/wppcolor.svg" alt=""> 
                </a>

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
