<template>
    <h1 class="
        leading-6 md:leading-[2.8rem]
        text-[22px] md:text-[24px] xl:text-[42px] 
        max-w-[45%] xl:max-w-[22%]
        tracking-tighter font-[SctoGroteskA] 
        uppercase mb-16 md:mb-32 xl:font-bold"
    >
        {{ heading }}
    </h1>
</template>

<script>
    export default {
        name: 'Heading',
        props: {
            heading: {
                type: String,
                required: true
            }
        }
    }
</script>

<style scoped>

</style>
