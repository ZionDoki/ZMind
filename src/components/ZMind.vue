<template>
  <div>
    <div id="mind-container"></div>
  </div>
</template>

<script>
import G6 from '@antv/g6'

const data = {
  id: "root",
  name: "123",
  children: [{
    id: "root2"
  }]
};

export default {
  name: "ZMind",
  methods: {
  },
  mounted() {

    const height = document.getElementById('mind-container').scrollHeight || window.innerHeight;
    const width = document.getElementById('mind-container').scrollWidth || document.body.clientWidth
    const graph = new G6.TreeGraph({
      container: 'mind-container',
      width,
      height,
      defaultNode: {
      },
      modes: {
        default: ['zoom-canvas', 'drag-canvas']
      },
      layout: {
        type: "mindmap"
      }
    });
    // graph.node(function(node) {
    //   return {
    //     label: node.id,
    //     labelCfg: {
    //       offset: 10,
    //       position: node.children && node.children.length > 0 ? 'left' : 'right',
    //     },
    //   };
    // });
    graph.data(data);
    graph.render();
    // graph.fitView();
  },
  
}
</script>

<style lang="stylus" scoped>

</style>