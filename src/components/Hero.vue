<template id="hero-body">
    <!-- <div  class="cursor bg-black w-3 h-3 rounded-full select-none pointer-events-none" data-cursor></div> -->
    <div class="wrapper">
       <div class="cursor bg-white w-[5rem] h-[5rem] rounded-full select-none pointer-events-none text-center text-[10px] font-[SctoGroteskA] font-bold flex xl:hidden justify-center items-center">WATCH<br>REEL</div>

       <div class="cursor-outline bg-white w-[8rem] h-[8rem] rounded-full select-none pointer-events-none text-center text-[13px] font-[SctoGroteskA] font-bold flex justify-center items-center" data-cursor-outline>WATCH<br>REEL</div>
    <video autoplay muted loop class="hero-vid" >
        <source src="../assets/media/hero-vid.mp4" type="video/mp4">
    </video> 
    </div>
    

</template>

<script>
import 'boxicons';

export default {
    name: "Hero",
   components: {
   },

   mounted() {
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
    .wrapper {
        transition: all 0.5s cubic-bezier(0.25, 1, 0.3, 1);
    transform-origin: 90% center;
    }
   .hero-vid {
    cursor: none;
    overflow: hidden;
    right: 0;
    bottom: 0;
    min-width: 100vw;
    min-height: 100vh;
    object-fit: cover;
   }

  .cursor-outline, .cursor {
    display: none;
    transition: 0.5s cubic-bezier(0.75, -1.27, 0.3, 2.33) transform, 0.2s cubic-bezier(0.75, -1.27, 0.3, 2.33) opacity;
    transform: translate(-50%, -50%);
    position: fixed;
    top: 50%;
    left: 50%;
   }

   .cursor {
    position: absolute;
    display: flex;
   }

   .cursor-outline::before, .cursor-outline::after, .cursor::before, .cursor::after {
    content: "BASIC/DEPT®";
    position: absolute;
    bottom: -30px;
    color: #fff;
   }

   .cursor::before {
    bottom: -20px;
   }

   .cursor-outline::after, .cursor::after {
    content: "2010-∞";
    bottom: -50px;
   }

   .cursor::after {
    bottom: -30px;
   }

   @media screen and (min-width: 600px) {
    .cursor-outline {
        display: flex;
    }

    .cursor {
        display: none;
    }
   }
</style>
