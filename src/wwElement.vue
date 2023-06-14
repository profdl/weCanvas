<template>
  <div class="canvas-element">
    <canvas ref="canvas" id="canvas"></canvas>
  </div>
</template>


<script>
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
    this.setupCanvas();
  },

 
};
</script>


