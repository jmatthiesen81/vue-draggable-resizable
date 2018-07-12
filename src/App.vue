<template>
  <div id="app">

    <VueDraggableFrame>
      <VueDraggableResizable :x="25" :y="25" :w="10" :h="5" :parent="true">
        <p>Component</p>
      </VueDraggableResizable>
      <VueDraggableResizable :x="70" :y="70" :w="5" :h="25" :parent="true">
        <p>Component</p>
      </VueDraggableResizable>
    </VueDraggableFrame>

    <!-- <div style="height: 500px; width: 500px; margin: 20px; border: 1px solid red; position: relative;">
      <VueDraggableResizable :x="50" :y="50" :w="400" :h="400" :parent="true">
        <p>Component</p>
      </VueDraggableResizable>
    </div>
    <div style="height: 500px; width: 500px; margin: 20px; border: 1px solid red; position: relative;">
      <h2>Grid 30x30</h2>
      <VueDraggableResizable :x="50" :y="50" :w="400" :h="400" :grid="[30, 30]" :parent="true">
      <p>Component</p>
      </VueDraggableResizable>
    </div>
    <div style="height: 500px; width: 500px; margin: 20px; border: 1px solid red; position: relative;">
      <h2>Custom handler</h2>
      <VueDraggableResizable :x="50" :y="50" :w="150" :h="50" :parent="true" :resizable="false" :dragHandle="'.dragHandle'">
        <p>Component</p>
        <span class="dragHandle">
          =
        </span>
      </VueDraggableResizable>
    </div>
    <div style="height: 500px; width: 500px; margin: 20px; border: 1px solid red; position: relative;">
      <h2>Grid 30x30 and handler</h2>
      <VueDraggableResizable :x="50" :y="50" :w="150" :h="50" :parent="true" :grid="[30, 30]" :resizable="false" :dragHandle="'.dragHandle'">
        <p>Component</p>
        <span class="dragHandle">
          =
        </span>
      </VueDraggableResizable>
    </div> -->
  </div>
</template>

<script>
import VueDraggableResizable from './components/vue-draggable-resizable'
import VueDraggableFrame from './components/vue-draggable-frame'

export default {
  name: 'app',
  components: {
    VueDraggableResizable,
    VueDraggableFrame
  }
}
</script>

<style>
  .active {
    border: 1px dashed black;
  }
  h2 {
    opacity: 0.3;
    padding: 0 0 0 20px;
    z-index: -1;
  }
  .dragHandle {
    position: absolute;
    top: 0;
    right: 0;
    padding: 5px;
    font-size: 20px;
    background-color: lightgrey;
  }
  .vdr {
    background: white;
  }
  .vdr-frame {
    background-color: rgb(190, 190, 190);
  }
</style>
