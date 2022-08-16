<template>
  <section class="section">
    <div class="workflow-panel">
      <div v-for="(nodes, index) in workflowNodes" :key="index" class="node-list">
        <p class="node-name">{{nodes.name}}</p>
        <div class="node-block" :style="{ 'background-color': nodes.imageColor }">
          {{ nodes.short_name }}
        </div>
        <p class="node-tag">{{ nodes.tag }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    workflowNodes: Array,
  },
};
</script>

<style></style>
