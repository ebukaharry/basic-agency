<template>
    <div id="items-container" ref="container" @mousedown="mouseIsDown"
         @mouseup="mouseUp" @mouseleave="mouseLeave" @mousemove="mouseMove">
      <!-- Your items here -->
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        startX: 0,
        scrollLeft: 0,
        isDown: false
      };
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
  