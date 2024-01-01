<script lang="ts" setup>
import { ref, onMounted } from "vue";
import grapesjs from "grapesjs";
import "grapesjs/dist/css/grapes.min.css";

const grapesCanvasRef = ref<HTMLElement>();

onMounted(() => {
  grapesjs.init({
    container: grapesCanvasRef.value,
    fromElement: true,
    storageManager: {
      type: "local",
      autosave: true,
      autoload: true,
    },
    canvas: {
      styles: [],
      scripts: [],
    },
  });
});
</script>

<template>
  <div ref="grapesCanvasRef"></div>
</template>
