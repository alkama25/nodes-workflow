<template>
  <div id="app">
    <nodes-panel @insertNode="insertNode"></nodes-panel>
    <workflow-panel :workflowNodes="workflowNodes"></workflow-panel>
  </div>
</template>

<script>
import NodesPanel from "./components/NodesPanel.vue";
import WorkflowPanel from "./components/WorkflowPanel.vue";

export default {
  name: "App",
  components: {
    NodesPanel,
    WorkflowPanel,
  },
  data() {
    return {
      workflowNodes: []
    };
  },
  methods: {
    insertNode(nodeDetail) {
      this.workflowNodes.push(nodeDetail)
    },
  },
};
</script>

<style lang="scss">
@import "./assets/scss/app.scss";
</style>
