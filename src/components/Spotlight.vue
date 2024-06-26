<template>
    <div class="md:flex md:flex-row-reverse justify-between xl:gap-28">
        <div class="spotlight-video w-[100%] md:w-[50%] max-h-[100%] mb-10 ">
            <video src="../assets/media/spotlight.mp4" autoplay muted loop></video>
        </div>
        <div class="spotlight-text md:w-[45%] lg:w-[45%] xl:w-[50%]">
            <h1 class="text-[40px] md:text-[46px] lg:text-[64px] xl:text-[6.55rem] tracking-tighter lg:tracking-[-0.08em] leading-[2.2rem] md:leading-[.9] lg:leading-[3.4rem] xl:leading-[5.8rem] font-[SctoGroteskA] font-semibold text-[#252422] uppercase">BASIC/DEPT® <br> helps brands ● connect w/ culture</h1>
            <h6 class="text-[15px] lg:text-[14px] xl:text-[19px] tracking-tighter leading-6 uppercase my-4 lg:mt-6 xl:my-6">adweek <span class="font-semibold font-[SctoGroteskA]">agency spotlight</span></h6>
            <div class="button xl:mt-20">
                <Button text="about us" link="#" />
            </div>
        </div>
    </div>
</template>

<script>
import Button from './Button.vue'

export default {
    name: 'Spotlight',
    components: {
        Button,
    }
}
</script>

<style scoped>

</style>
