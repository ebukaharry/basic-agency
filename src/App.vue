<script>
import Hero  from "./components/Hero.vue";
import Navbar from "./components/Navbar.vue";
import Separator from "./components/Separator.vue";
import Awards from "./components/Awards.vue";
import Overview from "./components/Overview.vue";
import FeaturedEngagements from "./components/FeaturedEngagements.vue";
import Spotlight from "./components/Spotlight.vue";
import FeaturedNews from "./components/FeaturedNews.vue";
import Footer from "./components/Footer.vue";

export default {
    name: "App",
    components: {
        Hero,
        Navbar,
        Separator,
        Awards,
        Overview,
        FeaturedEngagements,
        Spotlight,
        FeaturedNews,
        Footer,
    },
}
</script>

<template>
    <Hero />
    <Navbar />
    <Awards />
    <div class="px-5 md:px-10 lg:px-14 xl:px-20">
        <Separator />
    </div>
    <Overview />
    <div class="px-5 md:px-10 lg:px-14 xl:px-20">
        <Separator class="mb-28 xl:my-32 xl:mt-28"/>
    </div>
    <FeaturedEngagements />
    <!-- <Separator class="mb-12 mt-16 md:mt-16 md:mb-32 xl:mb-48" /> -->
    <div class="px-5 md:px-10 lg:px-14 xl:px-20">
        <Separator class="mb-12 mt-12 lg:mb-28 xl:my-32 xl:mt-28"/>
    </div>
    <div class="px-5 md:px-10 lg:px-14 xl:px-20">
        <Spotlight />    
        <FeaturedNews />
        <!-- <Separator class="mb-12 mt-16 md:mt-16 md:mb-48" /> -->
    </div>
    <Footer />
</template>

<style scoped>

</style>

