<template>
  <div class="single-node" @click="$emit('emitNode', nodeDetail)">
    {{ nodeDetail.name }}
  </div>
</template>

<script>
export default {
  props: {
    nodeDetail: Object,
    emitNode: Function,
  },
};
</script>

<style></style>
