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
        filebrowserBrowseUrl: 'http://localhost:8000/filemanager/dialog.php?type=1&editor=ckeditor&fldr=',
        filebrowerImageUploadUrl: 'http://localhost:8000/filemanager/dialog.php?type=2&editor=ckeditor'
      }
    }
  }
}
</script>

<style>

</style>