<template>
    <div id="header" class="nav text-[#f9cdcd] xl:text-white bg-[#252422] xl:bg-[transparent] py-3.5 xl:flex justify-between items-center px-5 xl:px-20 pt-4 xl:mt-10 ease-in-out" :class="[isOpen ? 'bg-[#252422]' : 'bg-[transparent]']">
        <div class="flex items-center gap-4 lg:gap-20 justify-between mt-3 md:mx-6 xl:mt-0 xl:mb-2 " >
            <img v-if="isOpen" src="../assets/media/logo-teal.svg" alt="logo" class="w-36">
            <svg v-else id="logo-svg" class="fill-white w-36" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 208.3 27.7"><path d="M0 24.1h11.7c5.5 0 8.7-2.3 8.7-6.8 0-2.8-1.7-4.5-4.1-5.3 2-.9 3.4-2.6 3.4-5.3 0-3.5-2.2-5.9-7.5-5.9H0zM13.1 7.9c0 1.6-1 2.4-3.2 2.4H6.4V5.5h3.5c2.2 0 3.2.8 3.2 2.4m.7 9c0 1.7-1 2.4-3.3 2.4H6.4v-4.9h4.2c2.2 0 3.2.8 3.2 2.5M38.2 24.1h6.7L36.8.7h-8.4l-8.1 23.4h6.5l1.2-3.8h9.1zM32.5 5.9l2.9 9.5h-5.9zM55.1 24.5c6.3 0 10.3-3 10.3-7.7 0-3.8-2.5-5.8-6.5-6.6l-5.1-1c-2-.4-2.6-1-2.6-2.1S52.4 5 54.5 5c2.4 0 4.1 1 4.2 3.1H65C65 2.5 60.3.3 54.5.3c-5.6 0-9.7 2.8-9.7 7.3 0 3.8 2.5 5.8 6.5 6.6l5.1 1c2 .4 2.6 1 2.6 2.1 0 1.5-1.4 2.3-3.7 2.3-2.6 0-4.5-1.3-4.6-3.8h-6.3c.2 5.5 3.7 8.7 10.7 8.7M67.3 24.1h6.4V.7h-6.4zM82 12.4c0-3.9 2.1-6.8 5.6-6.8 2.9 0 4.7 1.7 5.1 3.7h6.7C98.8 3.2 93.6.2 87.7.2 80 .2 75.4 5 75.4 12.3s4.5 12.1 12.3 12.1c6 0 11.2-2.9 11.8-9.1h-6.7c-.4 2.1-2.1 3.7-5.1 3.7-3.6.2-5.7-2.7-5.7-6.6M113.7 0h-5.2l-10 27.7h5.2zM137.8 12.4c0-6.6-3.6-11.7-12.8-11.7h-9.8v23.4h9.8c9.2 0 12.8-5.1 12.8-11.7m-6.6 0c0 4.6-2.6 6.3-6.2 6.3h-3.3V6.1h3.3c3.6 0 6.2 1.7 6.2 6.3M139.5 24.1H158v-5.3h-12.2v-4h10.7V9.7h-10.7V6.1h11.9V.7h-18.2zM180 8.9c0-5.9-3.8-8.1-9.6-8.1h-10.1v23.4h6.4V17h3.8c5.7 0 9.5-2.2 9.5-8.1m-6.6 0c0 2.3-1.1 3.2-3.7 3.2h-3.1V5.6h3.1c2.6 0 3.7 1 3.7 3.3M181 6.2h7.4v17.9h6.4V6.2h7.4V.7H181zM203.5 23.7c-2.6 0-4.8-2.1-4.8-4.8 0-2.6 2.1-4.8 4.8-4.8s4.8 2.1 4.8 4.8c0 2.6-2.2 4.8-4.8 4.8m0-8.8c-2.2 0-4 1.8-4 4s1.8 4 4 4 4-1.8 4-4-1.8-4-4-4"></path><path d="M204 17.2h-1.4v1.6h1.4c.5 0 .7-.3.7-.8s-.3-.8-.7-.8m-.1-.8c1.2 0 1.8.5 1.8 1.6 0 .6-.3 1.1-.9 1.3l1.2 1.8h-1.2l-1.1-1.6h-1.2v1.6h-1.1v-4.7z"></path></svg>
            <div class="menu xl:hidden text-white text-md font-bold"
             @click="toggleMenu()">
               <i v-if="isOpen" class="bx bx-x-circle bx-md"></i>
               <div v-else>MENU</div>
            </div>
        </div>
        <div class="xl:bg-[transparent] xl:static xl:flex lg:items-center mt-10 xl:mt-0 gap-4 py-6 xl:py-0 md:mx-5 xl:w-auto duration-700 ease-in-out relative h-dvh xl:h-auto  md:text-[24px] xl:text-sm text-xl uppercase font-[SctoGroteskA] " :class="[isOpen ? 'block' : 'hidden']">
            <p v-for="link in Links" 
               class="xl:mx-4 xl:my-0 my-4 md:mb-6">
                <a :href="link.link" :class="[isOpen ? 'block' : `${link.display}`]">{{ link.name }}</a>
            </p>
            <div :class="[isOpen ? 'block' : 'hidden']" class="absolute bottom-0" >
                <div class="wrapper copyright uppercase text-[#6d6c6c] text-[11px] py-5 flex justify-between">
                    <div class="mb-1">BASIC/DEPT®, Inc </div>
                    <div class="mb-1">10 - 24©</div>
                </div>
            </div>
        </div>
        <div class="cog hidden xl:block" @click="toggleInitiatives()">
            <i id="dots" class='bx bx-dots-horizontal-rounded text-white bx-md'></i>
            
        </div>
    </div>
    <!-- <div class="initiatives" >
        <div class="wrapper" v-if="initiativesOpen">
            <Separator class=""/>
        </div>
    </div> -->
</template>
<script>
import { ref, onMounted, onBeforeUnmount } from 'vue';
// import Separator from "./Separator.vue"
import 'boxicons';

export default {
    // components: {
    //     Separator,
    // },

    setup() {
        let isOpen = ref(false);
        let initiativesOpen = ref(false);

        let Links = [
            {
                name: "Work",
                link: "#"
            },
            {
                name: "About",
                link: "#"
            },
            {
                name: "News",
                link: "#"
            },
            {
                name: "Thinking",
                link: "#"
            },
            {
                name: "Careers",
                link: "#"
            },
            {
                name: "Contact",
                link: "#"
            },
            {
                name: "Initiatives >",
                link: "#",
                display: "hidden",
            }
        ]

        function toggleMenu() {
            isOpen.value = !isOpen.value;
        }

        function toggleInitiatives() {
            initiativesOpen.value = !initiativesOpen.value;
            console.log("american dream")
        }

          // Scroll behavior implementation
          onMounted(() => {
            let prevScrollpos = window.pageYOffset;
            
            const handleScroll = () => {
                const currentScrollPos = window.pageYOffset;
                const header = document.getElementById("header");
                const svg = document.getElementById("logo-svg");
                const cog = document.getElementById("dots");

                if (prevScrollpos > currentScrollPos) {
                    header.classList.remove("hide");
                    svg.classList.add("logo");
                    cog.classList.remove("text-white");
                    header.classList.add("navigation");

                } else {
                    header.classList.add("hide");
                    svg.classList.remove("logo");
                    cog.classList.add("text-white");
                    header.classList.remove("navigation");
                }
                prevScrollpos = currentScrollPos;
            };

            window.addEventListener('scroll', handleScroll);

            // Cleanup on component unmount
            onBeforeUnmount(() => {
                window.removeEventListener('scroll', handleScroll);
            });
        });

        return {
            Links,
            isOpen,
            initiativesOpen,
            toggleMenu,
            toggleInitiatives,
        }
    }
}
</script>
<style>
    #header {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        transition: top .3s ease-in-out;
    }

    #header.hide {
        top: -100px;
    }

    #header.navigation {
        
        color: #000;
    }

    #header svg.logo {
        fill: #000;
    }
</style>
