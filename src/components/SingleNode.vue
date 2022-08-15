<template>
  <div class="single-node">
    {{nodeDetail.name}}
  </div>
</template>

<script>
export default {
  props: {
    nodeDetail: {
      type: Object,
    },
  },
};
</script>

<style></style>
