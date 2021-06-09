<template>
  <div>
    <ckeditor value="Write your story" :config="cke4_config"></ckeditor>
  </div>
</template>

<script>
import Vue from 'vue'
import CKEditor from 'ckeditor4-vue';

Vue.use(CKEditor);

export default {
  name: "Ckeditor4",
  data() {
    return {
      cke4_config: {
        language: 'en',
        uiColor: '#aad5f0',
        filebrowserBrowseUrl: '/browser/browse.php',
        filebrowserImageUploadUrl: '/browser/upload.php'
      }
    }
  }
}
</script>

<style>

</style>