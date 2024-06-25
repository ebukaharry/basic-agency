<template>
    <footer class="px-5 md:px-10 lg:px-14 xl:px-20 mt-20 md:mt-40 xl:mt-[16rem] py-16 xl:py-28 xl:pr-[11rem] bg-[#252422] text-[#fff]">
       <div class="footer-heading flex flex-col items-start gap-14 xl:flex xl:flex-row justify-between">
            <img src="../assets/media/bd-logo-short.svg" alt="logo" class="h-4 xl:h-[22px]">
            <h2 class="text-[22px] xl:text-[32px] font-[SctoGroteskA] text-[#fff] leading-6 xl:leading-8 w-[80%] xl:w-[45%] tracking-tight">
                We collaborate with ambitious brands and people. Let's build.
                <span class="underline"><a href="mailto:biz@basicagency.com">biz@basicagency.com</a></span>
            </h2>
       </div>

       <div class="mt-20 xl:mt-32 xl:flex xl:justify-between xl:gap-">
           <div class="input relative mb-12 xl:w-[40%]">
                <h6 class="uppercase text-sm xl:text-lg font-[SctoGroteskA] leading-6 tracking-tight mb-3">Stay in the know</h6>
                <input type="email" placeholder="Email Address" class="text-input border-none text-sm xl:text-lg appearance-none outline-none pb-3 py-[.4em] bg-[transparent]">
                <button type="submit" name="submit" value="submit"><img src="../assets/icons/arrow-white.svg" alt="submit" class="absolute w-[1.2rem] h-[1.2rem] bottom-4 xl:top-12 right-0"></button>
            </div>

            <div class="links xl:flex xl:gap-32 xl:w-[45%]">
                <div>
                    <h6 class="uppercase text-sm xl:text-lg font-[SctoGroteskA] leading-6 tracking-tight mb-4">Social</h6>
                    <ul class="text-sm xl:text-lg">
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">Instagram</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">Twitter</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">LinkedIn</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">Facebook</a>
                        </li>
                    </ul>
                </div>
                <div class="mt-12 xl:mt-[inherit]">
                    <h6 class="uppercase text-sm xl:text-lg font-[SctoGroteskA] leading-6 tracking-tight mb-4">Initiatives</h6>
                    <ul class="text-sm xl:text-lg">
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">Crafted</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">Applied</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">Brandbeats</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">Moves</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">B®/Good</a>
                        </li>
                    </ul>
                </div>
                <div class="mt-12 xl:mt-[inherit]">
                    <h6 class="uppercase text-sm xl:text-lg font-[SctoGroteskA] leading-6 tracking-tight mb-4">Offices</h6>
                    <ul class="text-sm xl:text-lg">
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">San Diego - CA</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">New York - NY</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">Bay Area - CA</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">St. Louis - MO</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">Amsterdam - NL</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">London - EN</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">Berlin - GE</a>
                        </li>
                        <li class="leading-[1.3]">
                            <a href="" class="hover:underline">Argentina - AR</a>
                        </li>
                    </ul>
                </div>
            </div>
       </div>
    </footer>
    <div class="copyright px-5 xl:px-20  bg-[#191918] uppercase text-[#6d6c6c] text-center text-[11px] py-5 xl:flex xl:justify-between">
         <div class="mb-1">BASIC/DEPT®, Inc 10 - 24©</div>
         <div class="mb-1">Easy to understand, impossible to ignore.™</div>
         <div class="font-[SctoGroteskA]"><a href="">Terms</a>, <!-- --> <a href="">Privacy Policy</a></div>
     </div>

</template>
<script>
    export default {
        name: 'Footer'
    }
</script>
<style scoped>
    .text-input {
        border-bottom: 1px solid #fff;
        border-radius: .2em .2em 0 0;
        width: 100%;
    }

    .text-input:focus {
        border-bottom: 2px solid #fff;
    }

    .text-input::placeholder {
        color: #fff;
    }

    footer h6::before {
        margin-right: .5em;
        content: "●";
    }
</style>