<script setup>
import ImageDialog from './components/ImageDialog.vue'

// Sample data
const galleryItems = [
  {
    title: 'Title 1',
    type: 'data1',
    userData: 'https://sparc.science/',
  },
  {
    title: 'Title 2',
    type: 'data2',
    link: 'https://sparc.science/',
  },
  {
    title: 'Title 3',
    type: 'data3',
    link: 'https://sparc.science/',
  },
]
const iframeURL = '' // 'https://sparc.biolucida.net/image?c=NzQ5My1jb2wtMTkz'
const dialogOpen = true

defineProps({
  imageIframeURL: {
    type: String,
    default: ''
  },
  imageGalleryItems: {
    type: Array,
    default() {
      return []
    }
  },
  imageDialogOpen: {
    type: Boolean,
    default: true
  }
})
</script>

<template>
  <ImageDialog
    :imageIframeURL="iframeURL"
    :imageGalleryItems="galleryItems"
    :imageDialogOpen="dialogOpen"
  />
</template>

<style lang="scss">
#app {
  font-family: 'Asap', 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
  width: 100%;
  position: absolute;
}
</style>
