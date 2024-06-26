<template>
    <div class="overview-container pt-4 xl:py-12 mt-10 mb-12 md:mb-24 lg:mb-[8.5rem] xl:my-10">
       <div class="overview xl:flex mb-[9rem] md:mb-[14rem] lg:mb-[17.5rem] xl:mb-0 px-5 md:px-10 lg:px-14 xl:px-20">
            <div class="overview-text">
                <div class="text-[22px] tracking-tighter leading-[26px] xl:text-[38px] xl:leading-10 font-[SctoGroteskA] w-[100% md:w-[50%] xl:w-[70%] ">
                    BASIC/DEPT® is a global branding and digital design agency building products, services, and eCommerce experiences that turn cultural values into company value.
                </div>
                <div class="btn my-10 mb-14">
                    <Button text="see the work" />
                </div>
            </div>
            <img src="../assets/media/bd-logo.svg" alt="bd-logo" class="max-w-[60%] xl:max-w-[600px] h-[100%] float-right">
        </div> 
        <div class="brands flex justify-between pt-4 xl:pt-12 mt-20 xl:my-10 xl:mt-0 gap-5 md:gap-4 overflow-auto xl:overflow-hidden pl-5 md:pl-10 lg:pl-14 xl:px-20">
            <a href="#">
                <div class="img-container w-[280px] md:w-[350px] lg:w-[450px] xl:w-[500px]">
                    <div class="image overflow-hidden">
                        <img src="../assets/media/patagonia.webp" alt="patagonia">
                    </div>
                    <div class="img-text uppercase mt-3">
                        <h1 class="text-[22px] md:text-lg hover:underline font-semibold font-[SctoGroteskA] tracking-tighter">Patagonia</h1>
                        <p class="text-[10px] md:text-[11px] xl:text-[13px] font-[SctoGroteskA] pt-[0.4rem] xl:pt-[1.5rem] w-[100px] md:w-[230px]">
                            an ecommerce experience driven by patagonia's brand mission
                        </p>
                    </div>
                </div>
            </a>
            <a href="#" class="">
                <div class="img-container w-[280px] md:w-[350px] lg:w-[450px] xl:w-[500px]">
                    <div class="image overflow-hidden">
                        <img src="../assets/media/wilson.webp" alt="wilson">
                    </div>
                    <div class="img-text uppercase mt-3">
                        <h1 class="text-[22px] md:text-lg hover:underline font-semibold font-[SctoGroteskA]">Wilson</h1>
                        <p class="text-[10px] md:text-[11px] xl:text-[13px] font-[SctoGroteskA] pt-[0.4rem] xl:pt-[1.5rem] w-[100px] md:w-[230px]">
                            a century-old sports brand finding its place in culture
                        </p>
                    </div>
                </div>
            </a>
            <a href="#" class="">
                <div class="img-container w-[280px] md:w-[350px] lg:w-[450px] xl:w-[500px]">
                    <video autoplay loop muted src="../assets/media/google-store.mp4" alt="google-store"></video>
                    <div class="img-text uppercase mt-3">
                        <h1 class="text-[22px] md:text-lg hover:underline font-semibold font-[SctoGroteskA]">Google Store</h1>
                        <p class="text-[10px] md:text-[11px] xl:text-[13px] font-[SctoGroteskA] pt-[0.4rem] xl:pt-[1.5rem] w-[100px] md:w-[230px]">
                            an ecommerce experience helping google bring its hardware to people across the globe
                        </p>
                    </div>
                </div>
            </a>
        </div>
    </div>
    
</template>

<script>
import Button from "./Button.vue";

export default {
    name: "Overview",
    components: {
        Button,
    }
}
</script>

<style scoped>
    .brands::-webkit-scrollbar {
        display: none;
    }

    .image img {
        transition: transform 0.3s ease-out;
    }
    .image img:hover {
        transform: scale(1.05);
    }
</style>

