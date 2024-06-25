<template id="hero-body">
    <!-- <div  class="cursor bg-black w-3 h-3 rounded-full select-none pointer-events-none" data-cursor></div> -->
    <div class="cursor-outline bg-white w-[8rem] h-[8rem] rounded-full select-none pointer-events-none text-center text-[13px] font-[SctoGroteskA] font-bold flex justify-center items-center" data-cursor-outline>WATCH<br>REEL</div>
    <video autoplay muted loop class="hero-vid" >
        <source src="../assets/media/hero-vid.mp4" type="video/mp4" @mouseenter="handleMouseEnter">
    </video>

</template>

<script>
import 'boxicons';

export default {
    name: "Hero",
   components: {
   },

   mounted() {
    this.cursor = document.querySelector('[data-cursor]');
    this.cursorOutline = document.querySelector('[data-cursor-outline]');

    window.addEventListener('mousemove', this.handleMouseMove);
   },

   methods: {
    handleMouseMove(e) {
        this.mouseX = e.pageX;
        this.mouseY = e.pageY;

        this.cursorOutline.style.left = `${this.mouseX}px`;
        this.cursorOutline.style.top = `${this.mouseY}px`;

        cursorOutline.animate({
            left: `${this.mouseX}px`,
            top: `${this.mouseY}px`
        }, 
        {
            duration: 500,
            fill: 'forwards'
        })
    }
   }
}
   
</script>

<style scoped>
   .hero-vid {
    /* position: fixed; */
    cursor: none;
    overflow: hidden;
    right: 0;
    bottom: 0;
    min-width: 100vw;
    min-height: 100vh;
    object-fit: cover;
    /* opacity: 0.4; */
    transition: all 0.5s cubic-bezier(0.25, 1, 0.3, 1);
    transform-origin: 90% center;
   }

  .cursor-outline {
    transition: 0.5s cubic-bezier(0.75, -1.27, 0.3, 2.33) transform, 0.2s cubic-bezier(0.75, -1.27, 0.3, 2.33) opacity;
    transform: translate(-50%, -50%);
    position: fixed;
    top: 0;
    left: 0;
   }

   .cursor-outline::before, .cursor-outline::after {
    content: "BASIC/DEPT®";
    position: absolute;
    bottom: -30px;
    color: #fff;
   }

   .cursor-outline::after {
    content: "2010-∞";
    bottom: -50px;
   }
</style>
