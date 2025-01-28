<template>
    <div class="bg-white-screen ">
      <section class="max-w-5xl mx-auto py-10 sm:py-20" id="Preguntas">
        <div class="flex items-center justify-center flex-col gap-y-2 py-5">
          <h2 class="text-2xl md:text-3xl lg:text-4xl font-bold text-primary-black dark:text-gray-300">{{ sectionTitle }}</h2>
          <p class="text-lg font-medium text-primary-black dark:text-gray-300">{{ sectionSubtitle }}</p>
        </div>
        <div class="w-full px-7 md:px-10 xl:px-2 py-4">
          <div class="mx-auto w-full max-w-5xl border border-slate-400/20 rounded-lg bg-white dark:bg-gray-900"">
            <div
              v-for="(faq, index) in faqs"
              :key="index"
              :class="['border-b border-[#0A071B]/10', index === faqs.length - 1 ? '' : '']"
            >
              <button
                class="question-btn flex w-full items-start gap-x-5 justify-between rounded-lg text-left text-lg font-bold text-slate-800 dark:text-gray-300 focus:outline-none p-5"
                @click="toggleAnswer(index)"
              >
                <span class="text-primary-black dark:text-gray-300">{{ faq.question }}</span>
                <svg
                  stroke="currentColor"
                  fill="currentColor"
                  stroke-width="0"
                  viewBox="0 0 24 24"
                  :class="['mt-1.5 md:mt-0 flex-shrink-0 h-5 w-5 text-gray-500 dark:text-gray-300', faq.isOpen ? 'rotate-180' : '']"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path d="M16.293 9.293 12 13.586 7.707 9.293l-1.414 1.414L12 16.414l5.707-5.707z"></path>
                </svg>
              </button>
              <div
                v-if="faq.isOpen"
                class="answer pt-2 pb-5 px-5 text-sm lg:text-base text-gray-500 dark:text-gray-300 font-medium"
              >
                {{ faq.answer }}
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        sectionTitle: "Preguntas Frecuentes",
        sectionSubtitle: "Preguntas relacionadas con los sorteos",
        faqs: [
          {
            question: "¿Como puedo participar?",
            answer: "Puedes Participar uniendote al grupo de WhatsApp para adquirir tus numeros",
            isOpen: false,
          },
          {
            question: "¿Cuándo y a qué hora se realizará el sorteo?",
            answer: "Los sorteos se realizan diariamente o semanalmente en horas de la noche",
            isOpen: false,
          },
          {
            question: "¿Cómo garantizan la transparencia en el sorteo?",
            answer: "Somos una empresa con mas de dos años en el mercado con multiples clientes que respaldan nuestra transparencia",
            isOpen: false,
          },
          {
            question: "¿Cómo me entero si gano?",
            answer:
              "Una vez haya ganado se le contactara a traves de los datos integrados en el formulario",
            isOpen: false,
          },
        ],
      };
    },
    methods: {
      toggleAnswer(index) {
        this.faqs[index].isOpen = !this.faqs[index].isOpen;
      },
    },
  };
  </script>
  
  <style scoped>
  .rotate-180 {
    transform: rotate(180deg);
  }
  </style>
  