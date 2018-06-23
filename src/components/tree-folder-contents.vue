<template>
  <ul>
    <li v-for="(child, index) in children" :key="index">
      <tree-folder v-if="child.children" :folder="child"></tree-folder>
      <span v-else>{{child.name}}</span>
    </li>
  </ul>
</template>

<script>
  import TreeFolder from './tree-folder.vue'
  export default {
    props: ['children'],
    components: {
      TreeFolder
    }
  }
</script>
