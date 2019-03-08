<template>
  <div class="home">
    <editor-mce></editor-mce>
  </div>
</template>

<script>
// @ is an alias to /src
import EditorMce from '@/components/_tinymce.vue'

export default {
  name: 'home',
  components: {
    EditorMce
  }
}
</script>
