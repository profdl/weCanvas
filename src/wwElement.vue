<template>
  <div class="canvas-element">
    <canvas ref="canvas"></canvas>
  </div>
</template>

<script>
import { fabric } from 'fabric';

export default {
  mounted() {
    this.setupCanvas();
  },
  methods: {
    setupCanvas() {
      // Get canvas element using ref
      const canvasElement = this.$refs.canvas;

      // Create a new Fabric.js canvas
      this.canvasFabric = new fabric.Canvas(canvasElement);

      // Create a rectangle
      const rect = new fabric.Rect({
        left: 50,
        top: 50,
        fill: 'red',
        width: 100,
        height: 100
      });

      // Create a circle
      const circle = new fabric.Circle({
        left: 200,
        top: 200,
        fill: 'blue',
        radius: 50
      });

      // Add the shapes to the canvas
      this.canvasFabric.add(rect);
      this.canvasFabric.add(circle);

      // Render the canvas
      this.canvasFabric.renderAll();
    }
  }
};
</script>
