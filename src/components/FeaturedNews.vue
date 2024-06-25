<template>
    <div class="mt-36 md:mt-14 xl:mt-44">
        <div class="heading-wrapper flex justify-between mb-0">
            <Heading heading="Featured News" class="mb-[3rem] md:mb-[3rem]" />
            <Button text="View all" class="mt-2" />
        </div>

        <Separator class="mb-5 h-[1px]"/>
        <News v-for="news in articles" :news="news" />
    </div>
</template>

<script>
    import Heading from './Heading.vue';
    import Button from './Button.vue';
    import Separator from './Separator.vue';
    import News from './News.vue';

    export default {
        name: 'FeaturedNews',
        components: {
            Heading,
            Button,
            Separator,
            News,
        },
        data() {
            return {
                articles: [
                    {
                        img: 'https://cdn.sanity.io/images/8nn8fua5/production/e1ee6f1258bdc530b8843f97029f804856f72d61-2000x1468.jpg?w=720&fm=webp&q=65',
                        alt: 'news-1',  
                        date: '6.13.24',
                        title: 'The Future of Fashion and AI at Glossy\'s Ecommerce Summit',
                    },
                    // {
                    //     img: 'https://cdn.sanity.io/images/8nn8fua5/production/298d81bc795f2c46b55b8ca779d7c446326aeccd-1107x734.png?w=720&fm=webp&q=65',
                    //     alt: 'news-2',  
                    //     date: '6.3.24',
                    //     title: 'Retail\’s new playground: where physical meets digital',
                    // },
                    // {
                    //     img: 'https://cdn.sanity.io/images/8nn8fua5/production/1f72d719b320cc973839fabfd6cff390d3aac1c4-1000x734.jpg?w=720&fm=webp&q=65',
                    //     alt: 'news-3',  
                    //     date: '6.13.24',
                    //     title: 'Gen Alpha, the beta test for how brands can reach a new generation',
                    // },
                    {
                        img: 'https://cdn.sanity.io/images/8nn8fua5/production/8063a6f5ea9626cf98e092b801987075cf7fbe75-1000x734.jpg?w=720&fm=webp&q=65',
                        alt: 'news-4',  
                        date: '6.13.24',
                        title: 'What Sofia Coppola Can Teach Us About Shifting Culture',
                    },
                    {
                        img: 'https://cdn.sanity.io/images/8nn8fua5/production/289c0ed79c95e098d09f508e3fc1aa86c241e878-870x544.png?w=720&fm=webp&q=65',
                        alt: 'news-5',  
                        date: '6.13.24',
                        title: 'The 28TH Annual Webby Awards Nods Are In',
                        display: 'hidden',
                    },
                    // {
                    //     img: '',
                    //     alt: 'news-',  
                    //     date: '6.13.24',
                    //     title: '',
                    // },
                    // {
                    //     img: '',
                    //     alt: 'news-',  
                    //     date: '6.13.24',
                    //     title: '',
                    // },
                    // {
                    //     img: '',
                    //     alt: 'news-',  
                    //     date: '6.13.24',
                    //     title: '',
                    // },
                    // {
                    //     img: '',
                    //     alt: 'news-',  
                    //     date: '6.13.24',
                    //     title: '',
                    // },
                    // {
                    //     img: '',
                    //     alt: 'news-',  
                    //     date: '6.13.24',
                    //     title: '',
                    // },
                    // {
                    //     img: '',
                    //     alt: 'news-',  
                    //     date: '6.13.24',
                    //     title: '',
                    // },
                    // {
                    //     img: '',
                    //     alt: 'news-',  
                    //     date: '6.13.24',
                    //     title: '',
                    // },
                ]
            }
        }
    }
</script>

<style scoped>
    
</style>