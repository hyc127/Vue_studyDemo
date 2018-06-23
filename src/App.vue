<template>
  <div>
    <li v-for="(folder,index) in folders" :key="index">
      <tree-folder :folder="folder"></tree-folder>
    </li>
  </div>
</template>

<script>
  import TreeFolder from './components/tree-folder.vue'
  export default {
    data() {
      return {
        folders: [
          {
            name: 'folder-1',
            children: [
              {
                name: 'folder-1-1'
              },
              {
                name: 'folder-1-2',
                children: [
                  {
                    name: 'folder-1-2-1'
                  }
                ]
              }
            ]
          },
          {
            name: 'folder-2',
            children: [
              {
                name: 'folder-2-1',
                children: [
                  { name: 'folder-2-1-1' }
                ]
              }
            ]
          },
          {
            name: 'folder-3'
          }
        ]
      }
    },
    components: {
      TreeFolder
    }
  }
</script>
