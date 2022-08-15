<template>
  <div id="nodes-panel">
    <input
      type="search"
      placeholder="Add a new node.."
      @keyup.enter="filterNodes"
      v-model="searchTerm"
    />
    <div v-if="filterNodes.length">
      <single-node v-for="nodeItem in filterNodes" :key="nodeItem.id" :nodeDetail="nodeItem"></single-node>
    </div>
  </div>
</template>

<script>
import nodeListRecords from "../services/nodeListService";
import SingleNode from "./SingleNode.vue";
export default {
  components: {
    SingleNode,
  },
  data() {
    return {
      searchTerm: "",
    };
  },
  computed: {
    filterNodes() {
      if (this.searchTerm.length) {
        let results = nodeListRecords.filter((item) => {
          return item.name.toLowerCase().includes(this.searchTerm.toLowerCase());
        });
        return results;
      } else {
        return [];
      }
    },
  },
};
</script>

<style></style>
