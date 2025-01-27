<template>
    <section class="relative" id="Inicio">
        <div class="container flex flex-col md:grid gap-x-5 grid-rows-1 grid-cols-2 max-w-screen-xl content-center flex-wrap justify-center mt-48 mb-10 mx-auto items-center">
            <div class="mx-4">
                <img class="absolute -top-20 left-70 md:-top-20 md:left-40 w-[100px] h-[100px]  md:w-[220px] md:h-[220px] bg-no-repeat bg-center bg-contain" src="/src/assets/ticket6.svg">

                <div class="flex flex-col  p-4 ">
                    <h1 class="text-5xl m-2 md:text-5xl font-pop font-extrabold  text-primary-black">
                        The Clover Money..!
                    </h1>

                   
                </div>
                <div class="mt-6 flex flex-col p-4">
                    <p class="m-2 font-regular text-gray-500">
                        Bienvenidos a la plataforma líder en rifas y sorteos. Disfruta de sorteos diarios y semanales con premios increíbles.
                        Nos caracterizamos por nuestra seriedad, transparencia y compromiso, garantizando confianza y satisfacción en cada participación.
                        ¡Tu próxima gran oportunidad comienza aquí!
                    </p>
                </div>
                <div class="mx-auto p-4 ">
                    <a href="#_" class="box-border relative z-30 inline-flex items-center justify-center w-auto px-8 py-3 overflow-hidden font-bold text-white transition-all duration-500 bg-red-500 rounded-md cursor-pointer group ring-offset-2 ring-1 ring-red-300 ring-offset-red-200 ease focus:outline-none transform animate-pulseUpDown">
                    <span class="absolute bottom-0 right-0 w-8 h-20 -mb-8 -mr-5 transition-all duration-300 ease-out transform rotate-45 translate-x-1 bg-white opacity-20 group-hover:translate-x-0"></span>
                    <span class="absolute top-0 left-0 w-20 h-8 -mt-1 -ml-12 transition-all duration-300 ease-out transform -rotate-45 -translate-x-1 bg-white opacity-20 group-hover:translate-x-0"></span>
                    <span class="relative z-20 flex items-center text-sm">
                        Unete A Nuestro Grupo
                    </span>
                    <img class="w-12 h-12 me-2 ml-2" src="/src/assets/wppcolor.svg" alt=""> 
                </a>


                </div>
            </div>
            
            <div class="relative mb-20">
                <img class="absolute -bottom-30 -left-30  w-[100px] h-[100px]  md:w-[220px] md:h-[220px] bg-no-repeat bg-center bg-contain" src="/src/assets/ticket6.svg">
                <img class="absolute -top-35 -right-15 md:-top-30 md:-right-0  w-[100px] h-[100px]  md:w-[220px] md:h-[220px] bg-no-repeat bg-center bg-contain" src="/src/assets/ticket7.svg" >

                <div class="object-fill flex flex-col items-center p-2">
                    <!-- SVG superpuesto debajo de la imagen -->
                    <!-- <img class="absolute bottom-[-20px] " src="/src/assets/clover.svg" alt="image pattern"> -->
                    <img class="relative w-full md:w-96 md:h-96" src="/src/assets/clover.svg" alt="image description">
                    
                </div>
            </div>
        </div>
    </section>

    </template>
<style>
    @keyframes pulseUpDown {
        0% {
            transform: scale(1);
            box-shadow: 0px 10px 15px rgba(0, 0, 0, 0.1);
        }
        50% {
            transform: scale(1.05);
            box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.2);
        }
        100% {
            transform: scale(1);
            box-shadow: 0px 10px 15px rgba(0, 0, 0, 0.1);
        }
    }

    .animate-pulseUpDown {
        animation: pulseUpDown 2s infinite ease-in-out;
    }
</style>