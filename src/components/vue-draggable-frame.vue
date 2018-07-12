<template>
    <div ref="vdr-frame" :style="style" class="vdr-frame">
        <slot></slot>
    </div>
</template>

<script>
import { matchesSelectorToParentElements } from '../utils/dom'

export const VueDraggableFrame = {
  replace: true,
  name: 'VueDraggableFrame',
  props: {
    ratio: {
      type: Number,
      default: function () {
        return 16 / 9
      }
    }
  },
  methods: {},
  computed: {
    style: function (x) {
      return {
        'padding-bottom': 100 / this.ratio + '%'
      }
    }
  },
  watch: {}
}

export default VueDraggableFrame
</script>

<style scoped>
.vdr-frame {
    position: relative;
    width: 100%;
}
</style>
