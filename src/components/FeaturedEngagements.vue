<template>
    <div class="pl-5 md:pl-10 lg:pl-14 xl:pl-20 select-none">
        <Heading heading="Featured Engagements" class="mb-16 md:mb-14 lg:mb-28 max-w-[50.5%]" />

        <div
            class="brand-container flex justify-between gap-5 xl:gap-20 overflow-auto"
            ref="container"
            @mousedown="mouseIsDown"
            @mouseup="mouseUp"
            @mouseleave="mouseLeave"
            @mousemove="mouseMove"
        >
            <div 
                class="min-w-[75%] md:min-w-[45%] lg:min-w-[30.5%] xl:min-w-[23.5%] xl:mr-14" 
                v-for="brand in brands" 
                :key="brand.name"
            >
                <div class="img-container max-w-28">
                    <img :src="brand.img" :alt="brand.alt" :width="brand.width">
                    <div class="w-[22px] h-0.5 bg-[#252422] my-5"></div>
                </div>
                <div class="brand-details my-11 xl:mt-24">
                    <h1 class="text-lg xl:text-xl tracking-tighter xl:font-bold font-[SctoGroteskA] uppercase">
                        {{ brand.name }}
                    </h1>
                    <p class="desc pt-3 text-sm xl:text-lg font-[SctoGroteskA] tracking-tight">
                        {{ brand.desc }}
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import { ref } from 'vue';
    import Heading from './Heading.vue';

    export default {
        name: 'FeaturedEngagements',
        components: {
            Heading,
        },
        data() {
            return {
                startX: 0,
                scrollLeft: 0,
                isDown: false,

                brands: ref([
                    { 
                        name: 'Google', 
                        img: 'https://cdn.sanity.io/images/8nn8fua5/production/7121121ed910b145bdb6df487966a7888c2eb7c3-272x92.svg?w=720&fm=webp&q=65',
                        alt: 'Google',
                        desc: "Our embedded partnership with Google is as deep as it gets. We're the lead creative agency for Google Store and provide strategy, design, and prototyping to other divisions. Learn more about our partnership here."
                    },
                    { 
                        name: 'KFC', 
                        img: 'https://cdn.sanity.io/images/8nn8fua5/production/09a68ec6d03469bfd5bbb9726a58225acb900ae2-128x42.svg?w=720&fm=webp&q=65',
                        alt: 'KFC',
                        desc: "An award-winning global, digital transformation engagement spanning eCommerce, mobile app, and new drive thru experiences. Bringing KFC's brand story to life while making it easier for customers to buy chicken. Learn more about our partnership here." 
                    },
                    { 
                        name: 'Wilson', 
                        img: 'https://cdn.sanity.io/images/8nn8fua5/production/fbb650ce74c1849cb4da2d9951fad89149494cc9-171x42.svg?w=720&fm=webp&q=65',
                        alt: 'Wilson',
                        desc: "A reimagining of Wilson's brand visual identity, and brand campaign, to support a new product drop and the launch of the first brick and mortar retail location in the brand's 108-year history. Read our full case study here."
                    },
                    { 
                        name: 'AT&T', 
                        img: 'https://cdn.sanity.io/images/8nn8fua5/production/b2624b2d49d9c14eec0cd30203c5eec0331eac42-42x42.svg?w=200&fm=webp&q=65',
                        alt: 'AT&T',
                        desc: "Redesigning the digital flagship for the largest telecommunications company in the world. Creating frictionless paths to purchase for a wide range of consumers across a vast portfolio of products and services.",
                        width: '38%' 
                    },
                    { 
                        name: 'Patagonia',
                        img: 'https://cdn.sanity.io/images/8nn8fua5/production/8dd2f090726c8d5befeaa2924b44678e69452945-1024x200.svg?w=720&fm=webp&q=65',
                        alt: 'Patagonia',
                        desc: "Ongoing partnership providing strategy, branding, experience design, and development focused on bringing their mission and offerings to consumers through brand-led programs and platforms. Read our full case study here." 
                    }
                ])
            }
        },

        methods: {
            mouseIsDown(e) {
                this.isDown = true;
                this.startX = e.pageX - this.$refs.container.offsetLeft;
                this.scrollLeft = this.$refs.container.scrollLeft;
            },
            mouseUp(e) {
                this.isDown = false;
            },
            mouseLeave(e) {
                this.isDown = false;
            },
            mouseMove(e) {
                if (this.isDown) {
                e.preventDefault();
                
                // Move Horizontally
                const x = e.pageX - this.$refs.container.offsetLeft;
                const walkX = x - this.startX;
                this.$refs.container.scrollLeft = this.scrollLeft - walkX;
                }
            }
        }
    };
</script>

<style scoped>
    .brand-container::-webkit-scrollbar {
        display: none;
    }
</style>
