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
  <nav class="bg-emerald-100 border-b-[1px] border-black-medium dark:border-none dark:bg-gray-900">
    <div class="gap-y-2 flex flex-col md:max-w-screen-xl md:flex-row flex-wrap items-center justify-between mx-auto p-4">
      <a href="" class="flex items-center space-x-3 rtl:space-x-reverse">
        <span class="self-center text-primary-black text-2xl font-bold whitespace-nowrap dark:text-gray-300">The Clover</span>

        <img src="/src/assets/clover.svg" class="h-12" alt="Logo trebol">
      </a>
      <div class="flex flex-col md:flex-row items-center md:order-2 space-x-1 md:space-x-0 rtl:space-x-reverse">
               <div class="flex flex-row-">
                
              
          <img class="w-12 h-12 me-2 ml-2" src="/src/assets/money.svg" alt=""> 
          <img class="w-12 h-12 me-2 ml-2" src="/src/assets/moneyface.svg" alt=""> 
        </div>

        <!-- Botón de despliegue del menú -->
        <button
          id="theme-toggletwo"
          type="button"
          class="inline-flex  mt-4 items-center w-12 h-12 justify-center text-md text-primary-black rounded-lg md:hidden  focus:outline-none"
          @click="toggleMenu"
          :aria-expanded="isMenuOpen"
        >
          <span class="sr-only">Open main menu</span>
          <svg class="w-6 h-6" aria-hidden="true" fill="none" viewBox="0 0 17 14">
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
        <ul class="flex flex-col font-medium p-4 md:p-0 mt-4 border border-none md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0 items-center">
          <li v-for="item in menuItems" :key="item.href">
            <a :href="item.href" class="block py-2 px-3 text-primary-black md:p-0 dark:text-gray-300">
              {{ item.text }}
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
