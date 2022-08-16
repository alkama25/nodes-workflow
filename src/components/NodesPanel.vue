<template>
  <div id="nodes-panel">
    <input
      type="search"
      placeholder="Add a new node.."
      @keyup.enter="filterNodes"
      v-model="searchTerm"
    />
    <!-- Node list from mocked http response -->
    <div v-if="filterNodes.length">
      <single-node
        v-for="nodeItem in filterNodes"
        :key="nodeItem.id"
        :nodeDetail="nodeItem"
        @emitNode="emitNodeDetails"
      ></single-node>
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
  props: {
    insertNode: Function,
  },
  data() {
    return {
      searchTerm: "",
    };
  },
  computed: {
    // Filtered list of nodes on the basis of search query
    filterNodes() {
      if (this.searchTerm.length >= 2) {
        let results = nodeListRecords.filter((item) => {
          return item.name.toLowerCase().includes(this.searchTerm.toLowerCase());
        });
        return results;
      } else {
        return [];
      }
    },
  },
  methods: {
    emitNodeDetails(nodeValue) {
      this.$emit("insertNode", nodeValue);
    },
  },
};
</script>

<style></style>
