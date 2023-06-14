<template>
  <div class="canvas-element">
    <canvas ref="canvas"></canvas>
  </div>
</template>

<script>
import fabric from 'fabric';

export default {
  mounted() {
    this.initializeCanvas();
  },
  methods: {
    initializeCanvas() {
      this.canvas = new fabric.Canvas(this.$refs.canvas);

      // Create a rectangle object
      const rect = new fabric.Rect({
        left: 100,
        top: 100,
        fill: 'red',
        width: 20,
        height: 20
      });

      // Add the rectangle onto the canvas
      this.canvas.add(rect);
    },
    addRectangle() {
      // Create a rectangle object
      const rect = new fabric.Rect({
        left: 100,
        top: 100,
        fill: 'red',
        width: 20,
        height: 20
      });

      // Add the rectangle onto the canvas
      this.canvas.add(rect);
    }
  }
};
</script>
