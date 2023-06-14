<template>
  <div class="canvas-element">
    <canvas ref="canvas"></canvas>
  </div>
</template>

<script>
// I have no idea what I'm doing
export default {
  props: {
    content: { type: Object, required: true },
  },
  computed: {
    textStyle() {
      return {
        color: this.content.textColor,
      };
    },
  },
  mounted() {
    // Create a wrapper around the native canvas element
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
  }
};
</script>

<style lang="scss" scoped>
.my-element {
  p {
    font-size: 18px;
  }
}
</style>
