<template>
    <div class="vdr-frame">
        <slot></slot>
    </div>
</template>

<script>
import { matchesSelectorToParentElements } from '../utils/dom'

export const VueDraggableFrame = {
  replace: true,
  name: 'VueDraggableFrame',
  props: {},
  methods: {},
  computed: {},
  watch: {}
}

export default VueDraggableFrame;
</script>

<style scoped>
.vdr-frame {
    position: relative;
}
</style>
