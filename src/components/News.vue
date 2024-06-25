<template>
    <a href="#" class="news">
        <div class="news-item md:flex md:gap-5 md:mb-[3rem] xl:mb-[4.5rem] hover:underline cursor-pointer">
            <div class="news-img overflow-hidden md:max-w-[35%] xl:max-w-[494px] xl:max-h-[362px]">
                <img :src="news.img" :alt="news.alt" class="max-w-[100%] max-h-[100%]">
            </div>
            <div class="news-headline my-4 mb-10 md:my-0 md:flex md:flex-col md:justify-between">
                <div class="flex justify-between xl:gap-28">
                    <h3 class="text-[22px] md:text-[24px] xl:text-[42px] font-[SctoGroteskA] text-[#252422] leading-6 xl:leading-[2.5rem] tracking-tighter uppercase">{{ news.title }}</h3>
                    <img src="../assets/icons/arrow.svg" alt="arrow" class="arrow hidden md:block md:w-[2rem] md:h-[2rem] ml-[6rem] md:ml-[4rem]" ref="arrow">
                </div>
                <p class="hidden md:block md:text-[11px] xl:text-[14px] mb-[-5px] font-[SctoGroteskA] text-[#252422] tracking-tighter uppercase"><span class="font-bold font-[SctoGroteskA]">press </span> {{ news.date }}</p>
            </div>
            <div class="md:hidden news-date flex justify-between items-center my-4">
                <p class="text-[10px] md:text-[12px] font-[SctoGroteskA] text-[#252422] leading-6 tracking-tighter uppercase"><span class="font-bold font-[SctoGroteskA]">press </span> {{ news.date }}</p>
                <img src="../assets/icons/arrow.svg" alt="arrow" class="arrow w-[1.2rem] h-[1.2rem] md:w-[12px] md:h-[12px]">
            </div>
        </div>

        <Separator :class="news.display" class="mb-5 mt-1 md:10 h-[1px]"/>
    </a>
</template>
<script>
    import { gsap } from 'gsap'
    import Separator from './Separator.vue';
    export default {
        name: 'News',
        components: {
            Separator,
        },
       
        props: {
            news: {
                type: Object,
                required: true,
            }
        },

        mounted() {
            // gsap.to(this.$refs.arrow, { duration: 10, x: 100 });
        },
    }
</script>
<style>
    .news-img img {
        transition: transform 0.3s ease-out;
    }
    .news-img img:hover {
        transform: scale(1.05);
    }
    .arrow {
        transition: transform 0.5s ease-in-out;
    }
    .arrow:hover {
        transform: translateX(50%);
    }
</style>