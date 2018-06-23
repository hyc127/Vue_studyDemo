<template>
  <p>
    <span>{{folder.name}}</span>
    <tree-folder-contents :children="folder.children"></tree-folder-contents>
  </p>
</template>

<script>
  export default {
    props: ['folder'],

    beforeCreate() {
      this.$options.components.TreeFolderContents = () => import('./tree-folder-contents.vue')
    }
  }
</script>
