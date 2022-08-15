<template>
  <div id="app">
    <nodes-panel></nodes-panel>
    <workflow-panel></workflow-panel>
  </div>
</template>

<script>
import NodesPanel from './components/NodesPanel.vue'
import WorkflowPanel from './components/WorkflowPanel.vue'

export default {
  name: 'App',
  components: {
    NodesPanel,
    WorkflowPanel
  }
}
</script>

<style lang="scss">
@import "./assets/scss/app.scss";
</style>
